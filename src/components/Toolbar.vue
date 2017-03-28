<template  >
<div class="col-md-1" id="tool-bar">
    <i class="glyphicon glyphicon-list-alt"></i>
    <i class="glyphicon glyphicon-plus" @click="newNote"></i>
    <i class="glyphicon glyphicon-star-empty " :class="{starred: activeNote.favorite}" @click="favoriteNote"></i>
    <i class="glyphicon glyphicon-remove" @click="delNote"></i>
</div>
</template>

<script>
import {
    mapGetters,
    mapActions
} from 'vuex'
export default {
    computed: {
        ...mapGetters([
              'activeNote'
    ])
  },
    methods: {
        ...mapActions([
                "newNote",
                'delNote',
                'favoriteNote'
            ]
        )
}
}
</script>

<style lang="css">
#tool-bar {
    width: 80px;
    height: 100%;
    background-color: #30414D;
    color: #767676;
    padding: 35px 25px 25px 25px;
}
i {
    font-size: 30px;
    margin-bottom: 35px;
    cursor: pointer;
    opacity: 0.8;
    transition: opacity 0.5s ease;
}
.starred {
    color: #F7AE4F;
}
i:hover {
    opacity: 1;
}
</style>