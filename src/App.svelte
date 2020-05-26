<script>
  import "smelte/src/tailwind.css";
  //   import Button from "smelte/src/components/Button";
  import { Card, Button, Image } from "smelte";
  import { Checkbox, RadioButton, Switch, Icon } from "smelte";
  export let name;
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Visit the
    <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>
  <h6 class="mb-3 mt-6">Basic</h6>
  <div class="py-2">
    <Button>Button</Button>
  </div>

  <Card.Card>
    <div slot="title">
      <Card.Title
        title="The three little kittens"
        subheader="A kitten poem"
        avatar="https://placekitten.com/64/64" />
    </div>
    <div slot="media">
      <Image class="w-full" src="https://placekitten.com/300/200" alt="kitty" />
    </div>
    <div slot="text" class="p-5 pb-0 pt-3 text-gray-700 body-2">
      The three little kittens, they lost their mittens,
      <br />
      And they began to cry,
      <br />
      "Oh, mother dear, we sadly fear,
      <br />
      That we have lost our mittens."
    </div>
    <div slot="actions">
      <div class="p-2">
        <Button text>OK</Button>
        <Button text>Meow</Button>
      </div>
    </div>
  </Card.Card>

  <h5 class="pb-8 pt-10" id="checkboxes">Checkboxes</h5>

  <Checkbox label="A checkbox" />
  <Checkbox color="secondary" label="A colored checkbox" />
  <Checkbox disabled label="A disabled checkbox" />

  <h5 class="pb-8 pt-10" id="radio-buttons">Radio buttons</h5>

  <RadioButton
    name="test"
    items={[{ value: 1, label: 'One' }, { value: 2, label: 'Two' }]} />

  <RadioButton
    name="Colored test"
    color="blue"
    items={[{ value: 1, label: 'One' }, { value: 2, label: 'Two' }]} />

  <RadioButton
    name="test-disabled"
    disabled
    items={[{ value: 1, label: 'One' }, { value: 2, label: 'Two' }]} />

  <h5 class="pb-8 pt-10" id="switches">Switches</h5>

  <Switch />

  <Switch color="error" />
</main>
