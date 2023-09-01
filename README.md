# Phone_number_details
import phonenumbers
from phonenumbers import timezone,geocoder,carrier
number=input("Enter your number with your country code :")
phone=phonenumbers.parse(number)
time = timezone.time_zones_for_number(phone)
car = carrier.name_for_number(phone,"en")
data=geocoder.description_for_number(phone,"en")
geo=geocoder.country_name_for_number(phone,"en")
print("Phone Number and Country code is :",phone)
print("Time Zone :",time)
print("Telecom Operator :",car)
print("Country the number belongs to :", data)

