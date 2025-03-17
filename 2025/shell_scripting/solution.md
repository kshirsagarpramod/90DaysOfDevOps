**User creation**

	#!/bin/bash

				### User creation ###

	First_Arg=$1

	function Usercreation ( ) {

        if [ "$First_Arg" == "-r" ] || [ "$First_Arg" == "--reset" ]; then

        read -p "Please enter username to reset the password:" username
        validation=$(cat /etc/passwd | grep $username | wc -l)

                if
                        [ "$validation" == "0" ]; then

                        echo "$username user  is not present on the server"
                        exit
                else
			
			read -s "Please enter the new password:" newpassword
                        echo -e "$newpassword\n$newpassword" | sudo passwd "$username"
                      
		    if [ "$?" == "0" ]; then
			echo "Password for $username has been changed successfully."
		    else
			echo "Failed to change the Password for $username."		
	             fi

                fi

                elif [ "$First_Arg" != "-r" ] || [ "$First_Arg" != "--reset" ]; then
                echo "Invalid option Please user -r or --reset"

        fi

	}

	Usercreation



**User_Password_Reset**

	#!/bin/bash

				####  User_Password_Reset  ####

	First_Arg=$1

	function Userpasswordchange ( ) {

        	if [ "$First_Arg" == "-r" ] || [ "$First_Arg" == "--reset" ]; then

        	read -p "Please enter username to reset the password:" username
        	validation=$(cat /etc/passwd | grep $username | wc -l)

                	if
                       		 [ "$validation" == "0" ]; then

                        	echo "$username user  is not present on the server"
                        	exit
                	else

                        echo "Please enter the new password for $username"
                        read -s newpassword
                        echo -e "$newpassword\n$newpassword" | sudo passwd "$username"

                   		 if [ $? -eq 0 ]; then
                        	echo "Password for $username has been changed successfully."
                   		 else
                        	echo "Failed to change the Password for $username."
                     fi

                fi

                elif [ "$First_Arg" != "-r" ] || [ "$First_Arg" != "--reset" ]; then
                echo "Invalid option Please user -r or --reset"

        fi

	}

	Userpasswordchange



