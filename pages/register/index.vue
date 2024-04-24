<template>
    <div class="login">
        <div class="row ">
            <div class="logo col-6">
                <div class="left">
                    <h1>Shop Point</h1>
                    <p>
                        Gain data-based insignhts, view progess at a glance, and manage your
                        organization smarter
                    </p>
                    <img src="~/assets/images/login.webp" />
                </div>
            </div>
            <div class="form col-6">
                <div class="right">
                    <div class="title">
                        <h1>Welcome back!</h1>
                        <p>Etiam quis quam urna, Aliquam odio erat, accumsan eu nulla in</p>
                    </div>
                    <form>
                        <div class="mb-3">
                            <label for="exampleInputEmail1" class="form-label">Name</label>
                            <input type="name" class="form-control" aria-describedby="name" />
                        </div>
                        <div class="mb-3">
                            <label for="exampleInputEmail1" class="form-label">E-mail</label>
                            <input type="email" class="form-control" aria-describedby="emailHelp" />
                        </div>
                        <div class="mb-3">
                            <label for="exampleInputPassword1" class="form-label">Password</label>
                            <input type="password" class="form-control" />
                        </div>
                        <div class="forgot mb-3">Forgot PassWord?</div>

                        <button type="submit" class="btn btn-submit">Register</button>
                        <div class="line-container">
                            <div class="line"></div>
                            <div class="text">or</div>
                            <div class="line"></div>
                        </div>
                        <div class="btn-link ">
                            <button class="btn">
                                <img src="~assets/images/google.png" />
                                <nuxt-link class="link" to="/">Google</nuxt-link>

                            </button>
                            <button class="btn">
                                <img src="~assets/images/Facebook.png" />
                                <nuxt-link class="link" to="/">Facebook</nuxt-link>
                            </button>
                        </div>

                        <div class="account">
                            <p>you have an account? <nuxt-link to="/login">Sign in</nuxt-link></p>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>
<script>

import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
    layout: 'auth',
    setup() { },
})
</script>

<style lang="scss">
a {
    text-decoration: none;
}

@media screen and (max-width: 1285.60px) {
    .row {

        .btn-link {
            flex-wrap: wrap;

            .btn {
                width: 100%;
            }
        }

    }
}

@media screen and (max-width: 1024px) {
    .row {
        .logo {
            display: none;
        }

        .form {
            width: 100%;
        }

        .btn-link {

            flex-wrap: nowrap;

            .btn {
                /* width: 100%; */
                display: flex;
                gap: 10px;
                margin-bottom: 40px;
                justify-content: center;
                align-items: center;
            }
        }

    }
}


@media screen and (max-width: 768px) {
    .row {

        .btn-link {
            flex-wrap: wrap;

            .btn {
                width: 100%;
            }
        }

    }
}

.login {
    overflow: hidden;
}

.logo {
    background: #F9F9F9;

    .left {
        padding: 60px;
    }

    h1 {
        text-align: center;
        font-weight: bold;
    }

    p {
        font-size: 20px;
        font-weight: bold;
        opacity: 0.7;
    }

    img {
        width: 100%;
    }
}

.right {
    padding: 120px;

    .title {
        padding: 0 80px;

        h1 {
            text-align: center;
            font-weight: bold;
        }

        p {
            text-align: center;
        }
    }

    .forgot {
        text-align: center;
        color: blue;
        font-weight: 400;
    }

    .btn-submit {
        width: 100%;
        background: #00BA9D;
        border: 1px solid #01C8A9;
        box-shadow: 0 1px 10px rgba(2, 202, 171, 0.35);
        color: white;
        border-radius: 20px;
        line-height: 25px;
    }

    .line-container {
        gap: 5px;
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 15px 0;

        .line {
            margin: 30px 0;
            height: 1px;
            background: black;
            width: 100%;
            opacity: 0.1;
        }

        .text {
            font-size: 18px;
        }
    }



    .btn-link {
        display: flex;
        justify-content: space-between;
        gap: 10px;

        .btn {
            padding: 10px 70px;
            font-weight: bold;
            border: 1px solid blue;
            border-radius: 2rem;
            display: flex;
            gap: 10px;
            margin-bottom: 40px;
            justify-content: center;
            align-items: center;

            .link {
                text-decoration: none;
                color: black;
            }
        }
    }



    .account {
        text-align: center;
    }
}
</style>
