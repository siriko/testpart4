
# testpart4


package solid3;

import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

public class Smell1AlmostBestTest {

    @Test
    public void testZeroExponent() {
        assertEquals(1, new Smell1AlmostBest().toPower(5, 0));
    }

    @Test
    public void testPositiveExponent() {
        assertEquals(25, new Smell1AlmostBest().toPower(5, 2));
    }

    @Test
    public void testZeroBase() {
        assertEquals(0, new Smell1AlmostBest().toPower(0, 5));
    }

    @Test
    public void testOneBase() {
        assertEquals(1, new Smell1AlmostBest().toPower(1, 1000));
    }

    @Test
    public void testNegativeExponent() {
        assertThrows(ArithmeticException.class, () -> new Smell1AlmostBest().toPower(2, -2));
    }

    @Test
    public void testNegativeBaseEvenExponent() {
        assertEquals(4, new Smell1AlmostBest().toPower(-2, 2));
    }

    @Test
    public void testNegativeBaseOddExponent() {
        assertEquals(-8, new Smell1AlmostBest().toPower(-2, 3));
    }

    @Test
    public void testBaseZeroExponentZero() {
        // This could be undefined, depending on implementation
        assertEquals(1, new Smell1AlmostBest().toPower(0, 0));
    }

    @Test
    public void testLargeExponent() {
        assertEquals(1024, new Smell1AlmostBest().toPower(2, 10));
    }
}
