<template>
  <div
    :style="styleProps"
    class="l-shape-component"
    @click.prevent="handleclick"
    ></div>
</template>
<script lang="ts">
import { defineComponent } from "vue"
import useComponentCommon from "../../hooks/useComponentCommon"
import {transformToComponentProps, shapeDefaultProps, shapeStylePropsNames} from "../../defaultProps"
const defaultProps = transformToComponentProps(shapeDefaultProps)

export default defineComponent({
  name: 'l-shape',
  props: {
    ...defaultProps
  },
  setup (props) {
    const { styleProps, handleClick } = useComponentCommon(props, shapeStylePropsNames)
    return {
      styleProps,
      handleClick
    }
  }
})
</script>
