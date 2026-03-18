<template>
  <div class="commons-flex-col" style="margin-bottom: 16px">
    <label
      v-if="label"
      :for="id"
      class="modal-add-candidate-label commons-fs-14 commons-fw-500 commons-color-primary commons-flex-center"
    >
      {{ label }} <span v-if="required" class="modal-add-candidate-required">*</span>
    </label>
    <input
      :class="{'input-error': hasError } "
      :required="required"
      :id="id"
      :type="type"
      v-model="value"
      :placeholder="placeholder"
      class="modal-add-candidate-input commons-w-full commons-fs-14 commons-color-primary commons-outline-none commons-bg-white"
      
    />

    <span class="commons-fs-12" style="color: red; margin-top: 4px" >{{ errorMessage }}</span>
  </div>
</template>

<script setup>
// import { computed } from 'vue'
import { useField } from 'vee-validate'

// const dirty = ref(false)

const props = defineProps({
  modelValue: {
    type: [String, Number],
    default: '',
  },
  label: {
    type: String,
    default: '',
  },
  name: {
    type: String,
    required: true,
  },
  id: {
    type: String,
    default: '',
  },
  type: {
    type: String,
    default: 'text',
  },
  placeholder: {
    type: String,
    default: '',
  },
  required: {
    type: Boolean,
    default: false,
  },
  error: {
    type: String,
    default: '',
  },
})

const {value, errorMessage} = useField(() => props.name)

// const hasError = computed(() => {
//   return Boolean(props.error && dirty.value)
// })

// const emit = defineEmits(['update:modelValue'])

// const handleBlur = () => {
//   dirty.value = true
//   emit('blur')
// }
</script>

<style scoped>
.input-error {
  border: 1px solid red;
}
</style>