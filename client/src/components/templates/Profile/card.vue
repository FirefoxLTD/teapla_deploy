<template>
    <section class="card-list card">
      <figure class="card-image">
        <img src="https://images.unsplash.com/photo-1494253109108-2e30c049369b?crop=entropy&cs=srgb&fm=jpg&ixid=MnwxNDU4OXwwfDF8cmFuZG9tfHx8fHx8fHx8MTYyNDcwMTUwOQ&ixlib=rb-1.2.1&q=85" alt="An orange painted blue, cut in half laying on a blue background" />
      </figure>
      <div class="card-header">
        <a href="#">{{item.title}}</a>
        <button class="icon-button">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" display="block" id="Heart">
            <path d="M7 3C4.239 3 2 5.216 2 7.95c0 2.207.875 7.445 9.488 12.74a.985.985 0 0 0 1.024 0C21.125 15.395 22 10.157 22 7.95 22 5.216 19.761 3 17 3s-5 3-5 3-2.239-3-5-3z" />
          </svg>

        </button>
      </div>
      <div class="card-footer">
        <div class="card-meta card-meta--views">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" display="block" id="EyeOpen">
            <path d="M21.257 10.962c.474.62.474 1.457 0 2.076C19.764 14.987 16.182 19 12 19c-4.182 0-7.764-4.013-9.257-5.962a1.692 1.692 0 0 1 0-2.076C4.236 9.013 7.818 5 12 5c4.182 0 7.764 4.013 9.257 5.962z" />
            <circle cx="12" cy="12" r="3" />
          </svg>
          {{item.subject}}
        </div>
        <div class="card-meta card-meta--date">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" display="block" id="Calendar">
            <rect x="2" y="4" width="20" height="18" rx="4" />
            <path d="M8 2v4" />
            <path d="M16 2v4" />
            <path d="M2 10h20" />
          </svg>
          {{item.date}}
        </div>
      </div>
    </section>
</template>

<script>
export default {
  name: "card",
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

img {
  max-width: 100%;
  display: block;
}

.card-list {
  width: 90%;
  max-width: 400px;
  margin-right: 2rem;
  max-height: 440px;
}

.card {
  background-color: #FFF;
  box-shadow: 0 0 0 1px rgba(0, 0, 0, 0.05), 0 20px 50px 0 rgba(0, 0, 0, 0.1);
  border-radius: 15px;
  overflow: hidden;
  padding: 1.25rem;
  position: relative;
  transition: 0.15s ease-in;
}
.card:hover, .card:focus-within {
  box-shadow: 0 0 0 2px rgb(59 130 246), 0 10px 60px 0 rgba(0, 0, 0, 0.1);
  transform: translatey(-5px);
}

.card-image {
  border-radius: 10px;
  overflow: hidden;
}

.card-header {
  margin-top: 1.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.card-header a {
  font-weight: 600;
  font-size: 1.375rem;
  line-height: 1.25;
  padding-right: 1rem;
  text-decoration: none;
  color: inherit;
  will-change: transform;
  max-height: 55px;
  overflow: hidden;
}
.card-header a:after {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
}

.icon-button {
  border: 0;
  background-color: #fff;
  border-radius: 50%;
  width: 2.5rem;
  height: 2.5rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-shrink: 0;
  font-size: 1.25rem;
  transition: 0.25s ease;
  box-shadow: 0 0 0 1px rgba(0, 0, 0, 0.05), 0 3px 8px 0 rgba(0, 0, 0, 0.15);
  z-index: 1;
  cursor: pointer;
  color: #565656;
}
.icon-button svg {
  width: 1em;
  height: 1em;
}
.icon-button:hover, .icon-button:focus {
  background-color: #EC4646;
  color: #FFF;
}

.card-footer {
  margin-top: 1.25rem;
  border-top: 1px solid #ddd;
  padding-top: 1.25rem;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.card-meta {
  display: flex;
  align-items: center;
  color: #787878;
}
.card-meta:first-child:after {
  display: block;
  content: "";
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background-color: currentcolor;
  margin-left: 0.75rem;
  margin-right: 0.75rem;
}
.card-meta svg {
  flex-shrink: 0;
  width: 1em;
  height: 1em;
  margin-right: 0.25em;
}
</style>