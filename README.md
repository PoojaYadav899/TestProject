# TestProject
Test Repository

import java.math.BigDecimal;

public interface RevenueCalculator {
BigDecimal calculateRevenue(BigDecimal marginPercentage,BigDecimal costOfGoods);
}

class Revenue implements RevenueCalculator
{
	public static void main(String args[])
	{
		RevenueCalculator obj=new Revenue();
		System.out.println(obj.calculateRevenue(new BigDecimal(20),new BigDecimal(400)));	
	}
	private static final BigDecimal HUNDRED_BIGDECIMAL = new BigDecimal(100);
	public BigDecimal calculateRevenue(BigDecimal mp, BigDecimal cog)
	{	
		BigDecimal r=(HUNDRED_BIGDECIMAL.multiply(cog)).divide((HUNDRED_BIGDECIMAL.subtract(mp)));
	return r;
	}
}
