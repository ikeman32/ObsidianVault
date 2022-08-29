publish_it(){
    addall &&
    read -p 'comit message ' msg 
    commit "${msg}" &&
    push
}