# form_practice.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Creation</title>
        <style>
        .container_form{
            display: flex;
            justify-content: center;
        }
        form{
            width:  700px;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 7px;
            background-color: #f9f9f9;
        }
        h3{
            text-align: center;
            border: 1px solid rgb(180, 255, 226);
            background-color: rgb(194, 252, 230);
        }
        label{
            font-weight: bold;
        }
        
        input[type="text"], input[type="email"], input[type="number"] {
            width: 100%;
            padding: 8px;
            margin: 4px 0 12px;
            box-sizing: border-box;
        }
        form textarea{
            max-width: 100%;
            min-width: 100%;
            max-height: 60px;
            min-height: 60px;
        }
        button{
            font-family: sans-serif;
            font-weight: bold;
            border: 1px solid #9e9e9e;
            border-radius: 5px;
            padding: 5px;
            width: 60px;
            color: rgb(126, 126, 126);
        }
        button:hover{
            background-color: rgb(255, 255, 255);
            color: rgb(26, 26, 26);
            border: 1px solid rgb(39, 39, 39);
            border-radius: 5px;
            font-weight: bolder;
        }
        #namevalidation{
            color: red;
            font-size: 12px;
            display: none;
        }
        #emailvalidation{
            color: red;
            font-size: 12px;
            display: none;
        }
    </style>

</head>
<body>
    <div class="container_form">
        
        <form action="" name="form_sample" id="form_sample">
            <h3>Registration Form</h3><br><br>
            <label for="name">Full Name:</label>
            <input type="text" name="name" id="name" placeholder="Write your full name" onblur="FormValidation.nameValidation()">
            <div id="namevalidation">*Please enter a valid name.</div>
            <br>
            <label for="gender">Gender:</label>
            <label for="Male"><input type="radio" name="Gender" id="Male" value="Male">Male</label>
            <label for="Female"><input type="radio" name="Gender" id="Female" value="Female">Female</label>
            
            <br><br>

            <label for="subject">Subject:</label>
            <label for="Bangla"><input type="checkbox" name="subject" id="Bangla" value="Bangla">Bangla</label>
            <label for="English"><input type="checkbox" name="subject" id="English" value="English">English</label>
            <label for="Math"><input type="checkbox" name="subject" id="Math" value="Math">Math</label>
            <label for="ICT"><input type="checkbox" name="subject" id="ICT" value="ICT">ICT</label>
            
            <br><br>

            <label for="email">Email:</label>
            <input type="email" name="email" id="email" placeholder="Write your email..." onblur="FormValidation.emailValidation()"><br>
            <div id="emailvalidation">*Please enter a valid Email.</div>
            <label for="phone">Phone Number:</label>
            <input type="number" name="phone" id="phone">
            
            <br><br>

            <label for="city">City:</label>
            <select name="city" id="city">
                <option value="city">-Select City-</option>
                <option value="dhaka">Dhaka</option>
                <option value="chattogram">Chattogram</option>
                <option value="rajshahi">Rajshahi</option>
                <option value="khulna">Khulna</option>
                <option value="barishal">Barishal</option>
                <option value="sylhet">Sylhet</option>
                <option value="rangpur">Rangpur</option>
                <option value="mymensingh">Mymensingh</option>
            </select>
            
            <br><br>

            <label for="address">Address:<textarea name="address" id="address" cols="30" rows="1" placeholder="Write your address..."></textarea></label>
            
            <br><br>

            <button type="submit">Submit</button>
            <button type="reset">Reset</button>
        </form>

        <script src="form_practice.js"></script>
        <script>
            FormValidation.formSubmit();
        </script>
    </div>
</body>
</html>
