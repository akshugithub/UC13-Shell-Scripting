# Read the user input   
echo " Select the number "
echo " 1. number of days as input "
echo " 2. dates as input "

read number

case $number in 
        "1")
                echo " enter the days as input"
                read d


               error_exit()
                {
                   echo "Error: $1"
                   exit 1
                 }

                 find . -newermt "$d day ago" -exec du -h {} \;  || error_exit "enter the correct input"
                ;;
        "2")

echo "From date "  
read from
echo " to date "
read to

error_exit()
{
    echo "Error: $1"
    exit 1
}


find . -newermt "$from" -not -newermt "$to"  -exec du -h {} \; || error_exit "enter the correct input"
;;
esac
