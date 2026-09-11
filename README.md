# Fortune-cloud-task
# System IP address
ip addr show

# Network interface in use
route -n 

# Default gateway
ip route show

# DNS information
cat /etc/resolv.conf

# Get IPv4 address
ip -4 addr show

# Break IP into octets manually, 
echo "192.168.1.10" | tr '.' '\n'

# Check if private or public
ip a                 

# Private IP ranges for reference:
# 10.0.0.0    – 10.255.255.255
# 172.16.0.0  – 172.31.255.255
# 192.168.0.0 – 192.168.255.255

# Find IP of other devices on the network
arp -a


# --- On AWS Console ---
# 1. Launch EC2 instance: Amazon Linux 2 / Ubuntu AMI
# 2. Create/select a key pair (.pem file)
# 3. Configure Security Group to allow SSH (port 22)
# 4. Launch instance and note Public IPv4 address

# PS C:\Users\Shilpak> ssh -i .\Downloads\shilpak.pem ec2-user@52.72.133.6

# Find private IP
ip addr show
hostname -I

# Find public IP
curl ifconfig.me

# 1. Check IP address
ip addr show

# 2. Check network interface
ip link show

# 3. Check default route
route -n

# 4. Check network connectivity
ping -c 4 google.com
traceroute google.com

# 5. Check running services
sudo systemctl status nginx

# 6. Check listening ports
sudo netstat -tulnp

# 7. Check firewall/security rules (OS level)
sudo iptables -L -n -v

# --- Common fixes ---
# Service not running:
sudo systemctl start nginx

# Port blocked by OS firewall:
sudo firewall-cmd --reload
