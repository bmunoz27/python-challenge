import os
import csv

csvpath= os.path.join("..","Desktop","budget_data.csv")

monthly_changes = []
month_of_change=[]
row_count = 0
months_list=[]


with open(csvpath, 'r') as csvfile:
    csvreader = csv.reader (csvfile,delimiter =",")
    header = next(csvreader)
    for row in csvreader:
        
        profit_loss = int(row[1])
        months_list = row[0]
        monthly_changes.append(profit_loss)
        
monthly_sum = 0
for change in monthly_changes:
    monthly_sum += change
row_count= len(monthly_changes)

first=monthly_changes[0]
last= monthly_changes[85]
average_change=float((last-first)/(row_count-1))

monthly_changes.sort()   

positive=[]
negative=[]

for num in monthly_changes:
    if num >= 0:
        positive.append(num)
    else: 
        negative.append(num)

greatestincrease=[]
greatestdecrease=[]

greatestincrease= (positive[72])+ (-negative[4])
greatestdecrease= negative[0]-positive[65]

print("Financial Analysis")
print("-----------------------")
print("Total Months:", row_count)
print("Total: $",format(monthly_sum,",.2f"))
print("Average Change:$",round(average_change,2))
print("Greatest Increase in Profits:$", greatestincrease)
print("Greatest Decrease in Profits:$", greatestdecrease)

