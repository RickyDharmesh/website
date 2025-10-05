# Ex.07 Restaurant Website
# Date:05/10/2025
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:
```
urls.py
from django.contrib import admin
from django.urls import path
from food import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.restaurant,name="home"),
    path('administration/',views.administration,name='administration'),
    path('contact/',views.contact,name='contact'),
    path('about/',views.about,name='about'),
]

views.py 
from django.shortcuts import render

def restaurant(request):

    return render(request,'restaurant.html')

def administration(request):

    return render(request,'administration.html')


def contact(request):

    return render(request,'contact.html')


def about(request):

    return render(request,'about.html')

restaurant.html:

{% load static %}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RESTAURANT WEBSITE</title>

    <!-- <link rel="stylesheet" href="style.css"> -->
<style>
    * {
    margin: 0;
    padding: 0;
}

.title {
    text-align: center;
    padding: 19px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: xx-large;
    color: rgb(217, 18, 41);
}

.navbar {
    padding: 14px;
    display: inline-block;
    background-color: rgba(103, 103, 104, 0.747);
    color: #ffff;

}

ul,
li {
    display: inline;
    margin-left: 23px;
    padding: 100px;
    cursor: pointer;
}

li:hover {
    color: black;
}

/* offer start */
.offer {
    text-align: left;
    margin-top: 25px;
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: large;
    color: rgb(8, 1, 2);
    border-radius: 20px;
}

.offer {
    background-image: url("{% static 'Screenshot 2025-10-05 141652.png' %}");
    background-repeat: no-repeat;
    background-position: center;
    background-attachment: local;
    background-size: cover;

}

.offerhead {
    padding-top: 25px;
    padding-bottom: 50px;
}

/* menu */
.menu {
    text-align: center;
    padding: 50px;
    width: 50px;
    display: inline;
    margin-left: 150px;
}

.box1 {
    border-color: rgb(8, 12, 12);
    border-width: 3px;
    border-style: double;
    width: 350px;
    font-family: 'Times New Roman', Times, serif;
    background-color: rgba(103, 103, 104, 0.747);
    border-radius: 10px;
    display: inline-block;
}

.box1 h1 {
    text-align: left;
    font-family: sans-serif;
    font-size: xx-large;
    color: rgb(235, 235, 243);
}

.box2 {
    border-color: rgb(8, 12, 12);
    border-width: 3px;
    border-style: double;
    width: 350px;
    font-family: 'Times New Roman', Times, serif;
    background-color: rgba(103, 103, 104, 0.747);
    border-radius: 10px;
    display: inline-block;

}

.box2 h1 {
    text-align: left;
    font-family: sans-serif;
    font-size: xx-large;
    color: rgb(235, 235, 243);
}


.box3 {
    border-color: rgb(8, 12, 12);
    border-width: 3px;
    border-style: double;
    width: 350px;
    font-family: 'Times New Roman', Times, serif;
    background-color: rgba(103, 103, 104, 0.747);
    border-radius: 10px;
    display: inline-block;
}

.box3 h1 {
    text-align: left;
    font-family: sans-serif;
    font-size: xx-large;
    color: rgb(235, 235, 243);
}

/* ricky */

h5 {
    text-align: center;
}
</style>


</head>

<body>

    <h1 class="title"> RED DRAGON RESTAURANT

    </h1>

    <div class="navbar">

        <ul>
            <li>HOME</li>
            <li><a href="{% url 'administration' %}">ADMINISTRATION</a></li>
            <li><a href="{% url 'contact' %}">CONTACT US</a> </li>
            <li><a href="{% url 'about' %}">ABOUT US</a></li>
        </ul>

    </div>

    <div class="offer">

        <h1 class="offerhead">
            45% OFFER ON THIS MONTH
        </h1>

        <h4>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt consequatur minima, voluptatem quis quas
            amet perferendis deleniti officia veritatis laudantium suscipit culpa ipsum reprehenderit eum voluptatibus,
            beatae obcaecati. Incidunt accusantium ducimus ullam, ex, rem perspiciatis temporibus possimus quaerat autem
            nobis saepe corrupti debitis quos architecto mollitia nulla necessitatibus suscipit repudiandae!
        </h4>

    </div>

    <br>
    <br>



    <div class="menu">


        <div class="box1">

            <h1>
                OUR MENU
            </h1>

            <img src="{% static 'Screenshot 2025-10-05 144006.png' %}" height="150px">

            <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error perspiciatis consectetur quod! Saepe
                voluptatum, odio qui consequatur consequuntur, mollitia a culpa corporis fugiat beatae libero?

            </p>
        </div>

        <div class="box2">

            <h1>
                BOOK YOUR TABLE
            </h1>

            <img src="{% static 'Screenshot 2025-10-05 143744.png' %}" height="150px">

            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam culpa perspiciatis repudiandae
                aliquam distinctio debitis itaque, corporis laudantium id magni corrupti harum ducimus, dolor nesciunt.
            </p>


        </div>


        <div class="box3">

            <h1>
                TIMINGS
            </h1>

            <img src="{% static 'Screenshot 2025-10-05 141652.png' %}" height="150px">

            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae quia neque sapiente vitae enim iure?


            <ol>
                <li>TIME :</li>
                <li>8-2pm,5-11pm</li>

            </ol>

            </p>
        </div>
    </div>

    <br>
    <br>

    <hr>

    <br>

    <h5>
        DESIGNED AND DEVELOPED BY <i style="color: red;"> RICKY DHARMESH .P </i>

    </h5>




</body>

</html>

administration.html:
{% load static %}
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ADMINISTRATION PAGE</title>

    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body {
            background-color: rgb(202, 216, 111);
        }

        .title {
            text-align: center;
            padding: 19px;
            font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
            font-size: xx-large;
            color: rgb(217, 18, 41);
        }

        .navbar {
            padding: 14px;
            display: inline-block;
            background-color: rgba(103, 103, 104, 0.747);
            color: #ffff;

        }

        ul,
        li {
            display: inline;
            margin-left: 23px;
            padding: 100px;
            cursor: pointer;
        }

        li:hover {
            color: black;
        }

        .pic {
            text-align: center;

        }

        .one {
            padding: 50px;

        }

        .two {
            padding: 50px;

        }

        .three {
            padding: 50px;

        }

        .four {
            padding: 50px;

        }
    </style>
</head>

<body>
    <h1 class="title">  RED DRAGON  RESTAURANT</h1>

    <div class="navbar">

        <ul>
            <li><a href="{% url 'home' %}">HOME</a></li>
            <li>ADMINISTRATION</li>
            <li><a href="{% url 'contact' %}">CONTACT US</a> </li>
            <li><a href="{% url 'about' %}">ABOUT US</a></li>
        </ul>

    </div>

    <br>
    <br>

    <table class="pic">
        <tr>
            <h1 class="one">
               RED DRAGON  ADMINISTRATORS
            </h1>



        </tr>

        <tr>
            <td class="one">

                <img src="{% static 'male1.png' %}" height="250px">
                <h3>
                    Mr.Siddhu , CEO
                </h3>
            </td>

            <td class="two">

                <img src="{% static 'male2.png' %}" height="250px">
                <h3>
                    Mr.Harsath,President
                </h3>

            </td>

            <td class="three">

                <img src="{% static 'male3.png' %}" height="250px">
                <h3>
                    Mr.REVI,Senior Chef
                </h3>

            </td>

            <td class="four">

                <img src="{% static 'female.png' %}" height="250px">
                <h3>
                    Ms.Lathikha,Advisor
                </h3>

            </td>


        </tr>

    </table>


</body>

</html>

contact.html:
{% load static %}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CONTACT PAGE</title>

    <style>
        * {
            margin: 0;
            padding: 0;
        }
        body{
            background-color: rgb(127, 255, 168);
        }
        .title {
            text-align: center;
            padding: 19px;
            font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
            font-size: xx-large;
            color: rgb(217, 18, 41);
        }

        .navbar {
            padding: 14px;
            display: inline-block;
            background-color: rgba(103, 103, 104, 0.747);
            color: #ffff;

        }

        ul,
        li {
            display: inline;
            margin-left: 23px;
            padding: 100px;
            cursor: pointer;
        }

        li:hover {
            color: black;
        }

        .font{
            text-align: center;
            font-size: xx-large;
        }
    </style>
</head>

<body>
    <h1 class="title">  RED DRAGON RESTAURANT</h1>

    <div class="navbar">

        <ul>
             <li><a href="{% url 'home' %}">HOME</a></li>
            <li><a href="{% url 'administration' %}">ADMINISTRATION</a></li>
            <li>CONTACT US </li>
            <li><a href="{% url 'about' %}">ABOUT US</a></li>
            
        </ul>

    </div>



    <br>
    <br>


    <table class="font">
        <Tr>
            <td>Email:</td>
            <td>rickydharmesh@gmail.com</td>
        </Tr>

        <tr>
            <Td>Phone:</Td>
            <td>
                8679885963
            </td>
        </tr>
    </table>
</body>

</html>

about.html:
{% load static %}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ABOUT US PAGE</title>

    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body{
            background-color: aquamarine;
        }
        .title {
            text-align: center;
            padding: 19px;
            font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
            font-size: xx-large;
            color: rgb(217, 18, 41);
        }

        .navbar {
            padding: 14px;
            display: inline-block;
            background-color: rgba(103, 103, 104, 0.747);
            color: #ffff;

        }

        ul,
        li {
            display: inline;
            margin-left: 23px;
            padding: 100px;
            cursor: pointer;
        }

        li:hover {
            color: black;
        }

        p{
            font-size: medium;
            font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
        }
    </style>
</head>

<body>
    <h1 class="title">   RED DRAGON RESTAURANT</h1>

    <div class="navbar">

        <ul>
            <li><a href="{% url 'home' %}">HOME</a></li>
            <li><a href="{% url 'administration' %}">ADMINISTRATION</a></li>
            <li><a href="{% url 'contact' %}">CONTACT US</a> </li>
            <li>ABOUT US</li>
        </ul>

    </div>



    <br>
    <br>

    <h1 style="color: red;"> ABOUT RED DRAGON RESTAURANT</h1>

    <br>
    <br>


    <p>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eligendi omnis rem reprehenderit iusto vitae ad
        explicabo commodi doloremque ipsum eos, et impedit, facilis necessitatibus dolore fugit veniam alias, cumque qui
        distinctio quisquam perspiciatis voluptate minima laborum? Enim, expedita veritatis! Odio mollitia repellendus
        assumenda, rerum ad sequi, placeat dolorem eos fugiat facilis ipsam ex eius nemo repellat iusto voluptas modi
        exercitationem obcaecati consequatur enim quidem! Totam quibusdam voluptas cum distinctio eum soluta perferendis
        fuga doloribus quasi, eaque sint eveniet, minima quo voluptatem tempore dignissimos quis praesentium! Illum
        alias iusto harum qui quam dolores natus nisi perspiciatis sequi eligendi. Magni vel error quas dolor, atque
        natus. Ipsum laudantium ipsam facilis repellendus rerum debitis perferendis autem culpa iste sed sunt at dolore
        id, officia sint consequatur nostrum earum adipisci? Corrupti dolores beatae eos itaque delectus ex sed iusto.
        Voluptatem odit consequatur sunt reprehenderit doloremque qui, totam impedit, soluta obcaecati vitae voluptatum
        in quas quidem, incidunt magnam. Perferendis necessitatibus obcaecati dolores eum hic. Odit, eum iusto, ipsa
        officia repudiandae hic tempora dicta accusamus animi eos labore, reprehenderit fugit placeat. Officiis maiores
        eveniet sint quis culpa, praesentium modi nesciunt rerum natus dolor quisquam ipsa! Accusamus mollitia quo
        veniam corrupti, reiciendis quasi. Quis corrupti sit corporis molestiae quia. Unde vero temporibus cupiditate
        corporis ea. Laboriosam repudiandae, iure sint sunt tempore, repellat dolores molestiae dolorum consequatur nisi
        alias rem deserunt in ducimus dignissimos suscipit autem assumenda voluptatem magni? Odio accusantium quibusdam
        minus ipsam. Obcaecati, quod esse nulla odio consequatur deleniti, vitae debitis atque iusto sit facere
        voluptatum.
    </p>
    <br>
    <br>
<hr>

</body>

</html>

```
# OUTPUT:
![alt text](<../hotel/food/static/Screenshot 2025-10-05 171923.png>)
![alt text](<../hotel/food/static/Screenshot 2025-10-05 171935.png>)
![alt text](<../hotel/food/static/Screenshot 2025-10-05 172000.png>)
![alt text](<../hotel/food/static/Screenshot 2025-10-05 172117.png>)

# RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
