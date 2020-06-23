# python-challenge
#Beginning imports
import os
import csv

#Import the csv file
homework_csv = os.path.join("03-Python_Homework_Instructions_PyBank_Resources_budget_data.csv")

#Define a function to conduct an analysis

def data_analysis(PyBank_Homework):
    
    # Convert the data to the correct data types
    profit_loss = int(PyBank_Homework[1])
    
    #The total number of months included in the data set
    number_of_months = len(data) 

    #The net total amount of "Profit/Loss" over the period
    net_total = sum(data) 

    #The average of the changes in "Profit/Loss" over the period
    average_change = sum(data) / len(data)

    #The greatest increase in profits (date and amount) over the entire period
    greatest_increase = int(max(data))

    #The greatest decrease in losses (date and amount) over the entire period
    greatest_decrease = int(min(data))

#Open the csv file
with open(homework_csv) as csvfile:
    csvreader = csv.reader(csvfile, delimiter=",")
    csv_header = next(csvreader)

    #Store values as a data list
    data = []
    dt = []
    #Go through the rows for data
    for row in csvreader:
        # print(row)
        data.append(int(row[1]))
        dt.append(row[0])

#Print all of the data
print(f"Total Months: {number_of_months}"")
print(f"Net Total: {net_total}"")
print(f"Average Change: ${average_change}")
print(f"Greatest Increase: ${greatest_increase}")
print(f"Greatest Decrease: ${greatest_decrease}")
