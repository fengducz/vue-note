<template>
<div id="app">
    <div class="container-fluid">
        <div class="row">
            <Toolbar></Toolbar>
            <NotesList></NotesList>
            <Editor></Editor>
        </div>
    </div>
</div>
</template>

<script>
import store from './vuex/store'
import Toolbar from './components/ToolBar.vue';
import NotesList from './components/NotesList.vue';
import Editor from './components/Editor.vue';
export default {
    name: 'app',
    store,
    components: {
        Toolbar,
        NotesList,
        Editor
    }
}
</script>

<style>
html,
body,
.container-fluid,
.row,
#app {
    height: 100%;
}
</style>