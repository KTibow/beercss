<template lang="pug">
#steppers
  .large-space
  h4
    span Steppers
    a.chip.circle(
      @click="domain.showSamples(data, '#steppers > nav.scroll', 'Steppers', null, null)"
    )
      i code
  nav.wrap
    label.radio
      input(type="radio", name="color-steppers", checked, @click="domain.updateColor('#steppers button')")
      span default
    label.radio
      input(type="radio", name="color-steppers", @click="domain.updateColor('#steppers button', 'fill')")
      span fill
    label.radio
      input(type="radio", name="color-steppers", @click="domain.updateColor('#steppers button', '')")
      span primary
    label.radio
      input(type="radio", name="color-steppers", @click="domain.updateColor('#steppers button', 'secondary')")
      span secondary
    label.radio
      input(type="radio", name="color-steppers", @click="domain.updateColor('#steppers button', 'tertiary')")
      span tertiary
  .medium-space
  nav.scroll
    button.circle.small
      i done
    .maxhr
    button.circle.small 2
    .maxhr
    button.circle.small(disabled) 3
  .medium-space
  nav.scroll
    button.circle.small
      i done
    div Previous
    .maxhr
    button.circle.small 2
    div Current
    .maxhr
    button.circle.small(disabled) 3
    div Next
  .medium-space
  nav.scroll
    .center-align
      button.circle.small
        i done
      .small-margin Previous
    .maxhr
    .center-align
      button.circle.small 2
      .small-margin Current
    .maxhr
    .center-align
      button.circle.small(disabled) 3
      .small-margin Next
</template>

<script setup lang="ts">
import domain from "./domain";
import data from "./data";
</script>
