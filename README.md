using Microsoft.VisualStudio.TestTools.UnitTesting;
using System;

[TestClass]
public class ConverterTests
{
    [TestMethod]
    public void TestCase1()
    {
        float x = 0.0f;
        int expected = 1000;
        int result = Converter.Do(x);
        Assert.AreEqual(expected, result);
    }

    [TestMethod]
    public void TestCase2()
    {
        float x = 5.3f;
        int expected = 5;
        int result = Converter.Do(x);
        Assert.AreEqual(expected, result);
    }

    [TestMethod]
    [ExpectedException(typeof(ArgumentException))]
    public void TestCase3()
    {
        float x = 10.0f;
        int expected = -2000;
        int result = Converter.Do(x);
        Assert.AreEqual(expected, result);
    }

    [TestMethod]
    public void TestCase4()
    {
        float x = 15.8f;
        int expected = 10;
        int result = Converter.Do(x);
        Assert.AreEqual(expected, result);
    }

    [TestMethod]
    public void TestCase5()
    {
        float x = 30.2f;
        int expected = -2000;
        int result = Converter.Do(x);
        Assert.AreEqual(expected, result);
    }
}
