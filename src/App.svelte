<script>
  import { Route, Router } from "svelte-routing";
  import Main from "./routes/Main.svelte";
  import Error from "./lib/Error.svelte";
  import Form from "./routes/Form.svelte";
  export const url = "";
</script>

<Router {url}>
  <Route path="/" component={Main} />
  <!-- <Route path="/contacts" component={Main} /> -->
  <Route path="/form" component={Form} />
  <Route path="*" component={Error} />
</Router>
