#PF-Assgn-23
def calculate_bill_amount(gems_list, price_list, reqd_gems,reqd_quantity):
    bill_amount=0
    
    for i in range(0,len(reqd_gems)) :
      if reqd_gems[i] in gems_list: 
       for j in range(0,len(gems_list)):
          if gems_list[j]==reqd_gems[i]:
           bill_amount=bill_amount+ (reqd_quantity[i]*price_list[j])
      else:
           bill_amount=-1  
           break
             
    
    if bill_amount>30000:
        bill_amount=bill_amount-(bill_amount/20) 
    return bill_amount

gems_list=["Emerald","Ivory","Jasper","Ruby","Garnet"]

price_list=[1760,2119,1599,3920,3999]

#List of gems required by the customer
reqd_gems=["Ivory","Emerald","Garnet"]

#Quantity of gems required by the customer. reqd_gems and reqd_quantity have one-to-one correspondence
reqd_quantity=[3,10,12]
bill_amount=calculate_bill_amount(gems_list, price_list, reqd_gems, reqd_quantity)
print(bill_amount)
