# meow
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApplication5
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            double a = Convert.ToDouble(textBox1.Text);
            double b = Convert.ToDouble(textBox2.Text);
            double c = Convert.ToDouble(textBox3.Text);

            if (a == 0)
            {
                MessageBox.Show("Первый коэффициент равен нулю - решений нет! ", "Результат вычислений");

            }
            else {
                double D = b * b - 4 * a * c;
                if (D == 0)
                {
                    double x = (-b / (2 * a));
                    MessageBox.Show("Дискриминант равен нулю. Корень равен " + x + ".", "Результат вычислений");
                }
                if (D > 0)
                {
                    double x1 = ((-b - Math.Sqrt(D)) / (2 * a));
                    double x2 = ((-b + Math.Sqrt(D)) / (2 * a));
                    MessageBox.Show("Дискриминант равен " + D + ". Первый корень равен " + x1 + ". Второй корень равен " + x2 + ".", "Результат вычислений");
                }

                if (D < 0)
                {




                    double x1 = -Math.Sqrt(-D);
                    double x2 = +Math.Sqrt(-D);


                    MessageBox.Show("Дискриминант равен " + D + ". Первый корень равен " + -b / (2 * a) + +x1 / (2 * a) + "*i .   Второй корень равен " + -b / (2 * a) + "+" + x2 / (2 * a) + "*i", "Результат вычислений");
                }
            }
        }

        private void textBox1_KeyPress(object sender, KeyPressEventArgs e)
        {

            
            if (!(Char.IsDigit(e.KeyChar)))
            {
                if (e.KeyChar == '.' || e.KeyChar == ',' || e.KeyChar == '-' || e.KeyChar == (char)Keys.Back)
                {
                    if (e.KeyChar == (char)Keys.Back)
                    {

                    }
                    else
                        if (textBox1.Text.Contains(",") || textBox1.Text.Contains("."))
                    {
                        e.Handled = true;
                    }
                }
                else
                {
                    e.Handled = true;
                }
            }
        }

        private void textBox2_KeyPress(object sender, KeyPressEventArgs e)
        {
            if (!(Char.IsDigit(e.KeyChar)))
            {
                if (e.KeyChar == '.' || e.KeyChar == ',' || e.KeyChar == '-' || e.KeyChar == (char)Keys.Back)
                {
                    if (e.KeyChar == (char)Keys.Back)
                    {

                    }
                    else
                        if (textBox2.Text.Contains(",") || textBox2.Text.Contains("."))
                    {
                        e.Handled = true;
                    }
                }
                else
                {
                    e.Handled = true;
                }
            }
        }

        private void textBox3_KeyPress(object sender, KeyPressEventArgs e)
        {
            if (!(Char.IsDigit(e.KeyChar)))
            {
                if (e.KeyChar == '.' || e.KeyChar == ',' || e.KeyChar == '-' || e.KeyChar == (char)Keys.Back)
                {
                    if (e.KeyChar == (char)Keys.Back)
                    {

                    }
                    else
                        if (textBox3.Text.Contains(",") || textBox3.Text.Contains("."))
                    {
                        e.Handled = true;
                    }
                }
                else
                {
                    e.Handled = true;
                }
            }
        }
    }
    }


