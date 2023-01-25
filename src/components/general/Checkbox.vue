<template>
<div>
    <div class="checkbox-form">
        <div class="fields">
            <label 
                v-for="(option, i) of options"
                :key="i"
                class="option-item"
            >
                <span :for="option" class="labeltext">{{ option }}</span>
                <input 
                    :id="option"
                    type="checkbox"
                    v-model="checked"
                    :value="option"
                    @change="onChange"
                >
                <span class="checkmark" />
            </label>
        </div>
    </div>
</div>
</template>

<script lang="ts">
export default {
  props: {
    options: {
      type: Array,
      required: false,
      default: () => []
    }
  },
  data(){
    return {
      checked: []
    };
  },
  methods: {
    onChange() {
      this.$emit('input', this.checked);
    }
  }
};
</script>

<style>

.checkbox-form .fields {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 100%;
}

.checkbox-form input {
    position: absolute;
	opacity: 0;
	cursor: pointer;
	height: 0;
	width: 0;
}

.checkbox-form label {
    cursor: pointer;
    display: block;
    padding: 10px;
    position: relative;
    -webkit-user-select: none;
	-moz-user-select: none;
	-ms-user-select: none;
	user-select: none;
}

.checkbox-form .labeltext {
    font-size: 35px;
    font-family: 'Yuji Syuku', serif;
}

.checkbox-form .checkmark {
    background-image: url(../../assets/checkmark_aka.png);
    width: 64px;
    height: 64px;
    z-index: 100;
    position: absolute;
    opacity: 0;
    left: -5px;
    top: -5px;
    transition: 0.1s all;
}

.checkbox-form input:checked+.checkmark{
    opacity: 100;
}
</style>