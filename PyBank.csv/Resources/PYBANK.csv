import csv

file_path = 'PYBANK.csv'

months = []
profit_losses = []

with open(file_path, newline='') as csvfile:
    csvreader = csv.reader(csvfile)
    header = next(csvreader)
    
    for row in csvreader:
        months.append(row[0])
        profit_losses.append(int(row[1]))

'Calculate total number of months and net total'
total_months = len(months)
net_total = sum(profit_losses)

'Calculate changes in profit/losses'
changes = [profit_losses[i + 1] - profit_losses[i] for i in range(total_months - 1)]

'Calculate the average change'
average_change = sum(changes) / len(changes)

'Find the maximum and minimum changes'
max_increase = max(changes)
max_decrease = min(changes)

'Find the corresponding months for the maximum and minimum changes'
max_increase_month = months[changes.index(max_increase) + 1]
max_decrease_month = months[changes.index(max_decrease) + 1]

'Print the Results'
print("Financial Analysis")
print("----------------------------")
print(f"Total Months: {total_months}")
print(f"Total: ${net_total}")
print(f"Average Change: ${average_change:.2f}")
print(f"Greatest Increase in Profits: {max_increase_month} (${max_increase})")
print(f"Greatest Decrease in Profits: {max_decrease_month} (${max_decrease})")
