<template>
  <section>
    <Icon/>
    <div class="form-group">
      <span>ФИО</span>
      <input class="form-field" type="text" placeholder="Отображаемое имя">
    </div>
    <div class="form-group">
      <span>@</span>
      <input class="form-field" type="text" placeholder="Ссылка">
    </div>
    <div class="form-group">
      <span>#</span>
      <input class="form-field" type="email" placeholder="Статус">
    </div>
    <Button color="blue" text="Сохранить"/>
  </section>
</template>

<script>
import Icon from "./icon.vue"
import Button from "./button.vue"

export default {
  name: "Profile_Badge",
  components: {Icon, Button}
}
</script>

<style scoped>
/* :root {
  --input-color: #99a3ba;
  --input-border: #cdd9ed;
  --input-background: #fff;
  --input-placeholder: #cbd1dc;
  --input-border-focus: #275efe;
  --group-color: var(--input-color);
  --group-border: var(--input-border);
  --group-background: #eef4ff;
  --group-color-focus: #fff;
  --group-border-focus: var(--input-border-focus);
  --group-background-focus: #678efe;
} */

.form-field {
  display: block;
  width: 100%;
  padding: 8px 16px;
  line-height: 25px;
  font-size: 14px;
  font-weight: 500;
  font-family: inherit;
  border-radius: 6px;
  -webkit-appearance: none;
  color: #99a3ba;
  border: 1px solid #cdd9ed;
  background: #eef4ff;
  transition: border 0.3s ease;
}
.form-field::-moz-placeholder {
  color: #cbd1dc;
}
.form-field:-ms-input-placeholder {
  color: #cbd1dc;
}
.form-field::placeholder {
  color: #cbd1dc;
}
.form-field:focus {
  outline: none;
  border-color: #275efe;
  background-color: #ffffff;
}

.form-group {
  position: relative;
  display: flex;
  width: 100%;
}
.form-group > span,
.form-group .form-field {
  white-space: nowrap;
  display: block;
}
.form-group > span:not(:first-child):not(:last-child),
.form-group .form-field:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.form-group > span:first-child,
.form-group .form-field:first-child {
  border-radius: 6px 0 0 6px;
}
.form-group > span:last-child,
.form-group .form-field:last-child {
  border-radius: 0 6px 6px 0;
}
.form-group > span:not(:first-child),
.form-group .form-field:not(:first-child) {
  margin-left: -1px;
}
.form-group .form-field {
  position: relative;
  z-index: 1;
  flex: 1 1 auto;
  width: 1%;
  margin-top: 0;
  margin-bottom: 0;
}
.form-group > span {
  text-align: center;
  padding: 8px 12px;
  font-size: 14px;
  line-height: 25px;
  color: #99a3ba;
  background: #FFFFFF;
  border: 1px solid #99a3ba;
  transition: background 0.3s ease, border 0.3s ease, color 0.3s ease;
}
.form-group:focus-within > span {
  color: #ffffff;
  background: #678efe;
  border-color: #275efe;
}

body .form-group {
  max-width: 360px;
}
body .form-group:not(:last-child) {
  margin-bottom: 16px;
}
</style>