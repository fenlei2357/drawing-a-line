# drawing-a-line
using c# drawing a line
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace WindowsFormsApplication7
{
    public partial class Form1 : Form
    {
        int startX;     //获取鼠标起始点的X坐标
        int startY;    //获取鼠标起始点的Y坐标
        Graphics g;    //定义Graphics对象实例
        public Form1()
        {
            InitializeComponent();
        }
        private void Form1_Load(object sender, EventArgs e)
        {

            this.StartPosition = FormStartPosition.CenterScreen;

            this.BackColor = Color.Snow;

        }
        private void Form1_MouseDown(object sender, MouseEventArgs e)
        {
            startX = e.X;
            startY = e.Y;

        }
          private void Form1_MouseUp(object sender, MouseEventArgs e)
        {
            g = this.CreateGraphics();
            Pen p = new Pen(Color.Red, 4);
            g.DrawLine(p, startX, startY, e.X, e.Y);
            
        }
        private void radioButton1_CheckedChanged(object sender, EventArgs e)
        {

        }

        private void radioButton1_Click(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            this.Close();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            g = this.CreateGraphics();
            g.Clear(Color.Snow);
        }
    }
}
