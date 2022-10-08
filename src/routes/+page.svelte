<script lang="ts" >
  import { graphql } from '$houdini'

   let store = graphql`
query pokemons($first: Int!){
  pokemons(first: $first){
    id
    number
    name
    weight{
      minimum
      maximum
    }
    height{
      minimum
      maximum
    }
    classification
    types
    resistant
    weaknesses
    fleeRate
    maxCP
    maxHP
    image
  }
}
 `
</script>

{JSON.stringify($store)}
<!-- {#each $products.da<ta?.products ?? [] as product}
  <p>{product?.name}</p>
{/each} -->