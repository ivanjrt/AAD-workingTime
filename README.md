# copy paste the code and change the user name

```Ruby
$TrackUser =  "johndoe@somedomain.com"
 $onbFDate = (Get-AzureADUserExtension -ObjectId $TrackUser).Get_Item("createdDateTime")
 $onbDate  = ($onbFDate.split(" "))[0]
 $onbDateM = $onbDate.Split("/")[0]
 $onbDateD = $onbDate.Split("/")[1]
 $onbDateY = $onbDate.Split("/")[2]


 $TodaysDate  = Get-Date -Format "M/dd/yyy"
 $TodaysDateM = $TodaysDate.Split("/")[0]
 $TodaysDateD = $TodaysDate.Split("/")[1]
 $TodaysDateY = $TodaysDate.Split("/")[2]

 $yearD  = $TodaysDateY - $onbDateY
 $DayD   = $TodaysDateD - $onbDateD
 $monthD = $TodaysDateM - $onbDateM
 Write "Your Total Amount of work is been: $yearD Year(s), $monthD Month(s), and $DayD Day(s)"
  ```
