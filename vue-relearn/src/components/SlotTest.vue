<template>
    <div class="slot-test-container">
        <header>
            <slot name="slot-test-header"></slot>
        </header>
        <main>
            <slot name="slot-test-main"></slot>
        </main>
        <footer>
            <slot name="slot-test-footer"></slot>
        </footer>
        <!--    slot prop test   -->
        <span>
            <slot :user="user">
                {{ user.firstName }}
            </slot>
        </span>
    </div>
</template>

<script>
    export default {
        name: 'SlotTest',
        data () {
            return {
                user: {
                    firstName: 'firstName',
                    lastName: 'lastName'
                }
            }
        }
    }
</script>

<style scoped>

</style>