<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vermont Eligibility Check</title>
    <link rel="stylesheet" href="./framework/bootstrap.css">
    <link rel="shortcut icon" href="./logo (2).png" type="image/x-icon">
    <link rel="stylesheet" href="./framework/bootstrap-icons@1.4.1/font/bootstrap-icons.css">
    <link rel="stylesheet" href="./framework/all.css">
    <style>
    /* header Section................ */
        .header_main{
            width: 101%;
            height: 100%;
            background-image: linear-gradient(180deg, black, rgba(0, 0, 0, 0.356));
        }
        /* .header_img{
            height: 100%;
        } */
        .header_text{
            margin-left: 50px;
            margin-top: 10px;
            color: white;
            font-size: 30px;
            font-family: algerian, cooper black, Bahnschrift Condensed, sans-serif;
        }
        .prof_text{
            margin-top: 20px;
            text-align: center;
            font-family: Bodoni MT Black,cooper black, Bahnschrift Condensed, sans-serif;
        }

    /* Left Body Section.............. */
        .prof_img{
            margin-top: 20px;
            height: 100%;
            width: 100%;
            border-radius: 50%;
        }
        .prof_quote{
            text-align: center;
            font-family: Bahnschrift Condensed;
            margin-top: 7px;
            color: red;
            font-size: 20px;
        }
        .sub_body{
            background-color: beige;
            height: 100vh;
            width: 100%;
        }

    /* Right Body Section............. */
        .RB_main{
            margin-top: 20px;
            margin-left: 20px;
            background-color: rgba(255, 0, 0, 0.315);
            height: 100%;
            width: 90%;
            border-radius: 10px;
            box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
            padding: 20px;
        }
        .RB_cap{
            text-align: center;
            margin-top: 20px;
            font-family: Bodoni MT Black, cooper black, Bahnschrift Condensed, sans-serif;
        }
        .form-group1{
            margin-top: 40px;
            margin-bottom: 20px;
            margin-left: 20px;
        }
        .form-group2{
            margin-top: 20px;
            margin-bottom: 20px;
            margin-left: 20px;
        }
        label{
            font-family: Bahnschrift Condensed, sans-serif;
            font-size: 20px;
        }
        input, select{
            width: 80%;
            height: 40px;
            border-radius: 5px;
            font-family: Bahnschrift Condensed, sans-serif;
            margin-top: 10px;
            margin-bottom: 10px;
            padding-left: 10px;
        }
        input:focus, select:focus{
            outline: none;
            border: 2px solid green;
        }


        .elig_butt{
            margin-top: 10px;
            background-color: rgba(0, 0, 0, 0.781);
            color: white;
            font-family: Bahnschrift Condensed, sans-serif;
            width: 250px;
            margin-top: 30px;
        }
        .elig_butt:hover{
            background-color: green;
            color: white;
            font-family: Bahnschrift Condensed, sans-serif;
            width: 250px;
            margin-top: 30px;
        }
        .res_out{
            margin-top: 30px;
            text-align: center;
            font-family: Bahnschrift Condensed, sans-serif;
        }
        
        /* Footer................................ */
        .foot_er{
            background-image: linear-gradient(180deg, black, rgba(0, 0, 0, 0.356));
            color: white;
            text-align: center;
            padding: 10px;
            font-family: Bahnschrift Condensed, sans-serif;
        }
        .foot_er p{
            margin-top: 20px;
        }

        @media screen and (max-width: 760px){
            .prof_img{
                width: 50%;
                height: 50%;
                margin-left: 50px;
            }
            .header_text{
                font-size: 20px;
                margin-left: 20px;
            }
            .sub_body{
                height: 150vh;
            }
            .RB_main{
                width: 100%;
                height: 100%;
                margin-left: 0px;
            }
            .prof_img{
                width: 70%;
                height: 70%;
            }
            
        }
    </style>
</head>
<body>
<!-- Header Section........................................... -->
    <header>
        <div class="row header_main">
            <img src="./logo (2).png" alt="My Logo" class="header_img">
            <p class="header_text">
                Confirm Availability of Fund to Qualify for University of Vermont
            </p>
        </div>

    </header>
<!-- Main Body Section......................................... -->
    <div class="container-fluid sub_body">
        <div class="row">
    <!-- left body section...................................... -->
            <div class="col-md-4">
                <h2 class="prof_text">
                    Profile of User
                </h2>
                <div>
                    <img src="./My Profile.jpg" alt="My Picture Display" class="prof_img">
                </div>
                <p class="prof_quote">Education is the passport to the future,<br> 
                    for tomorrow belongs to those <br>
                    who prepare for it today </p>
            </div>
    <!-- Right body section..................................... -->
            <div class="col-md-8">
                <div class="RB_main">
                    <h3 class="RB_cap">Click Button to Check for Availability of Adequate Fund</h3>
            
                    <!-- <form action="" method="post"> -->
                        <div class="form-group1">
                            <label for="fund" class="form-label">How Many Sources of Fund(s) do You Have?</label><br>
                            <select class="form-select" id="fund" required>
                                <option value="" disabled selected>Select an Option</option>
                                <option value="null">null</option>
                                <option value="one">1</option>
                                <option value="two">2</option>
                                <option value="three">3</option>
                                <option value="more">More</option>
                            </select><br>
                        </div>
                        <div class="form-group2">
                            <label for="amount">Please, Input the Total Amount you have from all souurces </label><br>
                            <input type="number" name="amount" id="amount" placeholder="Enter Amount in Naira">
                        </div>
                        <center>
                        <button type="submit" onclick="compare()" class="btn elig_butt">Check Eligibility</button>
                        </center>
                    <!-- </form> -->
                    <div id="result" class="res_out"></div>
                </div>

            </div>
        </div>
    </div>

    <script src="./framework/bootstrap@5.0.0/bootstrap.js"></script>
    <script>
        function compare(){
            var fund = document.getElementById("fund").value;
            var amount = document.getElementById("amount").value;
            var result = document.getElementById("result");

            if(fund === "null" || amount === ""){
                result.innerHTML = "<h3 style='color:red;'>Please, Select an Option and Input Amount</h3>";
            } else if(fund === "one" && amount >= 20000000){
                result.innerHTML = "<h3 style='color:green;'>Congratulations! You are Eligible to Apply for University of Vermont</h3>";
            } else if(fund === "two" && amount >= 10000000){
                result.innerHTML = "<h3 style='color:green;'>Congratulations! You are Eligible to Apply for University of Vermont</h3>";
            } else if(fund === "three" && amount >= 5000000){
                result.innerHTML = "<h3 style='color:green;'>Congratulations! You are Eligible to Apply for University of Vermont</h3>";
            } else if(fund === "more" && amount >= 2000000){
                result.innerHTML = "<h3 style='color:green;'>Congratulations! You are Eligible to Apply for University of Vermont</h3>";
            } else {
                result.innerHTML = "<h3 style='color:red;'>Sorry! You are Not Eligible to Apply for University of Vermont</h3>";
            }
        }
    </script>
</body>

<!-- footer Section............................................. -->
<footer>
    <div class="foot_er">
        <p>Copyright &copy; 2025 All Rights Reserved | Designed by Okonkwo Ugochukwu</p>
    </div>
</footer>
</html>
