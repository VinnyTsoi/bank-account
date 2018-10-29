'''A Python class that can be used to create and manipulate a personal bank account (VT - 28 Oct 2018)'''
class BankAccount(object):
  
  balance = 0
  
  def __init__(self, name):
    self.name = name
    
  def __repr__(self):
    return "%s's account. Balance: %.2f" % (self.name, self.balance)
    #return "Bank Account Name: %s \nBank Account Balance:  %.2f" % (self.name, self.balance)
  
  
  def show_balance(self):
    print "Bank Account Balance: %.2f" % (self.balance)
    print
    
  def deposit(self, amount):
    if amount <= 0:
      print 'Invalid amount'
      print
      return
    else:
      print 'Deposited: %.2f' % (amount)
      self.balance += amount
      self.show_balance()
      
  def withdraw(self, amount):
    if amount > self.balance:
      print 'Invalid amount'
      print
      return
    else:
      print "You are withdrawing %.2f" % (amount)
      self.balance -= amount
      self.show_balance()
      
my_account = BankAccount("Victor")
  
print my_account.__repr__()
  
my_account.show_balance()
  
my_account.deposit(2000)
  
my_account.withdraw(500)
  
print my_account.__repr__()
  
  
      
    
  
  
  
  