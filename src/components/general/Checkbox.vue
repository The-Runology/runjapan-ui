<template>
<div>
    <div class="checkbox-form">
        <div :class="[
            'fields',
            'd-flex',
            layoutDirection === 'row' ? 'flex-row' : 'flex-column']">
            <label 
                v-for="(option, i) of options"
                :key="i"
                class="option-item"
                ref="options"
            >
                <span :for="option" :class="['labeltext', textDirection === 'col' ? 'd-block' : '']" :style="{
                  fontSize: fontSize + 'px',
                  width: textDirection === 'col' ? fontSize * 1.4 + 'px' : '0'
                }">{{ option }}</span>

                <input 
                    :class="'option-' + i"
                    type="checkbox"
                    :value="option"
                    @change="onChange(i)"
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
    },
    exlusive: {
      type: Boolean,
      required: false,
      default: false
    },
    layoutDirection: {
      type: String,
      required: false,
      default: "row"
    },
    textDirection: {
      type: String,
      required: false,
      default: "row"
    },
    fontSize: {
      type: Number,
      default: 35
    }
  },
  data(){
    return {
      checked: Array<Number>()
    };
  },
  methods: {
    onChange(index: number) {
      
      if (this.exlusive) {
        for (let i = 0; i < this.checked.length; ++i) {
          this.removeCheck(this.checked[i]);
        }
        this.checked = []
      }

      this.checked.push(index);
      this.$emit('input', this.checked);
    },
    removeCheck(index: Number) {
      this.$refs.options[index].getElementsByClassName('option-'+index)[0].checked=false
    },
    mounted() {
      
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
    transition: 0.2s all;
}

.checkbox-form input:checked+.checkmark{
    opacity: 100;
}

.checkmark.hide {
  opacity: 0 !important;
}

</style>