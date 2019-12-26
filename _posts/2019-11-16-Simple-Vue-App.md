---
layout: post
title:  "Enum"
date:   2019-11-16
comments: true
categories: Vue
---
#### Simple Vue App


Vuex structure

#### api : actual api functions that triggers changes in state
- login() : login to imgur with pre-defined client_id
- fetchImages(token) : get images from imgur with authorizing token
- uploadImages(images, token) : post images to imgur with authorizing token

#### components : components that make up one view in index.html
- AppHeaderVue: template + script + css, export name, computed, methods
    mapActions and mapGetters from vuex



#### store : defines state, getters, actions, and mutations
auth.js
    - state : fetches imgur token and store it in token variable
    - getters: isLoggedIn tells whether there is a state or not. If there is, it is 1 (!state.token == 0 and !0 == 1)
    - actions: 
        logout() : renders token null (? what is commit)
        login() : calls api.login()
        finalizeLogin() : ?
    -mutations : setToken(state, token), sets the state of token to be token
images.js
    - state : array of images[]
    - getters : get 'allImages' from state
    - actions : 
        fetchImages
        uploadImages

    - mutations : 


#### index.js
#### App.vue : main vue file that gathers components
#### main.js : main js file that creatse vue object, sets vue router and directs vue to use vue router.

