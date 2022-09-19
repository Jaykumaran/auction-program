# auction-program
from replit import clear
print('''


                         ___________
                         \         /
                          )_______(
                          |"""""""|_.-._,.---------.,_.-._
                          |       | | |               | | ''-.
                          |       |_| |_             _| |_..-'
                          |_______| '-' `'---------'` '-'
                          )"""""""(
                         /_________\
                         `'-------'`
                       .-------------.
                      /_______________\



''')
print("Welcome to auction")
bids={}
bidding_finished=False
def high_bid(bidding_record):
  highest_bid =0
  winner=""
  for bidder in bidding_record:
    bid_amount= bidding_record[bidder]
    if bid_amount> highest_bid:
      highest_bid=bid_amount
      winner=bidder
  print(f"the winner is {winner} with a highest bid of {highest_bid}")
while not  bidding_finished:
  name=input("What is your name: ")
  price= int(input("What is your bid? $: "))
  declaration=input("are there any other bidders? Type 'yes' or 'no': ")
  bids[name]=price
  if declaration=="no":
    bidding_finished=True
    high_bid(bids)
  elif declaration=="yes":
    clear()
 

