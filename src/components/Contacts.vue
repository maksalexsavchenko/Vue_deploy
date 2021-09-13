<template>
    <div class="contacts">
        <div class="container">
            <div class="text_block">
                <h1 class="title">Contact us!</h1>
                <p class="text">The support staff and customer service are available to help you with any questions or needs you might have. Just drop us a line.</p>
                <h3 class="desc">This site is owned and operated by Kode Tech Solutions LTD</h3>
                <div class="contact_text">
                    <h4 class="title">Phone:</h4>
                    <p class="desc">442038857261</p>
                </div>
                <div class="contact_text">
                    <h4 class="title">Email:</h4>
                    <p class="desc">help@google.com</p>
                </div>
                <div class="contact_text">
                    <h4 class="title">Address:</h4>
                    <p class="desc">Trust Company Complex, Ajeltake Road, Ajeltake Island, Majuro, Republic of the Marshall Islands, MH 96960</p>
                </div>
            </div>
            <div class="form_block">
                <input type="text" placeholder="Name">
                <input type="text" placeholder="E-mail">
                <textarea name="text" placeholder="Message" id="" cols="30" rows="10"></textarea>
                <div class="btn">Send</div>

            </div>

        </div>
    </div>
</template>

<script>
    export default {
        name: "Contacts"
    }
</script>

<style lang="scss">
    .contacts{
        margin-top: 140px;
        background: #EFEDFF;
        padding: 120px 0;
        .container{
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;
            .text_block{
                max-width: 500px;
            }
            .form_block{
                background: white;
                border: 2px solid #6248FF;
                border-radius: 20px;
                padding: 80px;
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                align-items: center;

                input{
                    border: 1px solid #E0E0E0;
                    color: #828282;
                    border-radius: 3px;
                    padding: 7px 16px;
                    font-size: 16px;
                    margin-bottom: 24px;
                    max-width: 425px;
                    width: 100%;
                    &:focus{
                        border: 1px solid #828282;
                        color: #4F4F4F;
                        outline: none;
                    }
                }
                textarea{
                    border-radius: 3px;
                    outline: none;
                    border: 1px solid #E0E0E0;
                    color: #828282;
                    padding: 7px 16px;
                    font-size: 16px;
                    resize: none;
                    margin-bottom: 40px;
                    max-width: 425px;
                    width: 100%;
                    &:focus{
                        border: 1px solid #828282;
                        color: #4F4F4F;
                        outline: none;
                    }
                }
            }
        }
    }
</style>