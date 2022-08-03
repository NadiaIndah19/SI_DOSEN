<script>
export default {
  name: 'Default',

  middleware({ route, redirect }) {
     return redirect('/admin/dashboard')
  }
}
</script>
