# B-MAC-Address

package mac.compB;

import java.net.InetAddress;
import java.net.NetworkInterface;
import java.net.SocketException;
import java.net.UnknownHostException;

    public class macadd{
       
        public static void main(String[] args){
        
        InetAddress IP;
        try {
          
          //tries to connect to DNS to get IP Address and hostname
          IP = InetAddress.getLocalHost();
          System.out.println("Company B-IP Address:  " + IP.getHostAddress());
          
          NetworkInterface networkB = NetworkInterface.getByInetAddress(IP);
          
          //MAC Address
          byte[] macb = networkb.getHardwareAddress();
          
          System.out.println("Company B - MAC address : ");
          
          StringBuilder sbB = new StringBuilder();
		for (int b = 0; b < macb.length; b++) {
			sbB.append(String.format("%02X%s", macB[b], (a < macB.length - 1) ? "-" : ""));		
          }
          
          System.out.println(sbB.toString());
        
} catch (UnknownHostException e) {
		
		e.printStackTrace();
		
	} catch (SocketException e){
			
		e.printStackTrace();
			
	}
  }
 }
