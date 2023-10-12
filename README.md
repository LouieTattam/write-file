# write-file




# Open reading file
file = open('devices-01.txt', 'r')


# Read 
# file one line at a time and remove whitespace
name = file.readline().strip()
ip_address = file.readline().strip()
os_type = file.readline().strip()
username = file.readline().strip()
password = file.readline().strip()


# Display using string format

print('---Device info formatted-----------------------------------------------------')
print('')
print('Name      IP address      OS        Username        Password')
print('{0:8} {1:15}  {2:8}  {3:10}  {4:10}'.format(name, ip_address, os_type, username, password))

print('')
print('-------------------------------------------------------------------------------')




# Create comma-seperated string of device information attributes

device_info = name
device_info = device_info + ',' + ip_address
device_info = device_info + ',' + os_type
device_info = device_info + ',' + username
device_info = device_info + ',' + password



# Write device information
print('')
print('--- Writing device information to file ----------------------')
print('')
outfile = open('devices-01-out.csv', 'w')
outfile.write(device_info)
outfile.write('\n')
print('--- Device information written to file -----------------------')
print('')




infile = open('devices-01-out.csv', 'r')
device_info = infile.readline().strip()
infile.close()




# Display information

print('')
print('---Device info read from file we wrote -------------------')
print('')
print('Device Info: ', device_info)
print('')
print('----------------------------------------------------------')
print('')
