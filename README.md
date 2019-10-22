# How-to-count-non-zero-pixels
import cv2
import matplotlib as plt


class image:
    img = cv2.imread('lft_0.bmp')
    gray = grayscaled = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
    # img2 = cv2.rectangle(img1, (200,300), (1900,1400), (0,0,255), 5)
    retval, threshold = cv2.threshold(gray, 127, 255, cv2.THRESH_BINARY)
    nonzero1 = None
    nonzero2 = None
    nonzero3 = None
    nonzero4 = None
    nonzero5 = None

    # nzCount = cv2.countNonZero(img1)
    # print("No of non zero in image", nzCount)
    def image_left_top(self):
        # img = self.threshold[830:906, 447:755]
        img = self.threshold[861:899, 472:742]
        #cv2.imshow("ff1", img)
        self.nonzero1 = cv2.countNonZero(img)
        #print("No of non zero in image", self.nonzero1)
        cv2.imwrite('./leftjy/top//left/image_left_top.bmp', img)

    def top_left_circle(self):
        img2 = self.threshold[887:977, 625:710]
        #cv2.imshow("ff2", img2)
        self.nonzero2 = cv2.countNonZero(img2)
        #print("No of non zero in image2", self.nonzero2)
        cv2.imwrite('./leftjy/top/left/top_left_circle.bmp', img2)

    def bottom_left_circle(self):
        img3 = self.threshold[1312:1405, 597:701]
        #cv2.imshow("ff3", img3)
        self.nonzero3 = cv2.countNonZero(img3)
        #print("No of non zero in image3", self.nonzero3)
        cv2.imwrite('./leftjy/top/left/bottom_left_circle.bmp', img3)

    def top_right_0(self):
        # img4 = self.threshold[839:922, 937:1223]
        img4 = self.threshold[868:914, 943:1211]
        #cv2.imshow("ff4", img4)
        self.nonzero4 = cv2.countNonZero(img4)
        #print("No of non zero in image4", self.nonzero4)
        cv2.imwrite('./leftjy/top//right/top_right_0.bmp', img4)

    def top_right_circle_0(self):
        img5 = self.threshold[902:986, 965:1049]
        #cv2.imshow("ff5", img5)
        self.nonzero5 = cv2.countNonZero(img5)
        #print("No of non zero in image5", self.nonzero5)
        cv2.imwrite('./leftjy/top/right/top_right_circle_0.bmp', img5)

    def right_bottom_circle(self):
        img6 = self.threshold[1326:1414, 948:1034]
        #cv2.imshow("ff6", img6)
        self.nonzero6 = cv2.countNonZero(img6)
        #print("No of non zero in image6", self.nonzero6)
        cv2.imwrite('./leftjy/top/right/right_bottom_circle.bmp', img6)




class image2:
    img = cv2.imread('2parts.bmp')
    gray = grayscaled = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
    # img2 = cv2.rectangle(img1, (200,300), (1900,1400), (0,0,255), 5)
    retval, threshold = cv2.threshold(gray, 127, 255, cv2.THRESH_BINARY)
    nonzero11 = None
    nonzero12 = None
    nonzero13 = None
    nonzero14 = None
    nonzero15 = None

    # nzCount = cv2.countNonZero(img1)
    # print("No of non zero in image", nzCount)
    def image_left_top(self):
        # img = self.threshold[830:906, 447:755]
        img = self.threshold[861:899, 472:742]
        #cv2.imshow("ff7", img)
        self.nonzero11 = cv2.countNonZero(img)
        #print("No of non zero in image11", self.nonzero11)
        cv2.imwrite('./leftjy/top/left1/image_left_top.bmp', img)

    def top_left_circle(self):
        img2 = self.threshold[887:977, 625:710]
        #cv2.imshow("ff8", img2)
        self.nonzero12 = cv2.countNonZero(img2)
        #print("No of non zero in image12", self.nonzero12)
        cv2.imwrite('./leftjy/top/left1/top_left_circle.bmp', img2)

    def bottom_left_circle(self):
        img3 = self.threshold[1312:1405, 597:701]
        #cv2.imshow("ff9", img3)
        self.nonzero13 = cv2.countNonZero(img3)
        #print("No of non zero in image13", self.nonzero13)
        cv2.imwrite('./leftjy/top/left1/bottom_left_circle.bmp', img3)

    def top_right_0(self):
        # img4 = self.threshold[839:922, 937:1223]
        img4 = self.threshold[868:914, 943:1211]
        #cv2.imshow("ff10", img4)
        self.nonzero14 = cv2.countNonZero(img4)
        #print("No of non zero in image14", self.nonzero14)
        cv2.imwrite('./leftjy/top/right1/top_right_0.bmp', img4)

    def top_right_circle_0(self):
        img5 = self.threshold[902:986, 965:1049]
        #cv2.imshow("ff11", img5)
        self.nonzero15 = cv2.countNonZero(img5)
        #print("No of non zero in image15", self.nonzero15)
        cv2.imwrite('./leftjy/top/right1/top_right_circle_0.bmp', img5)

    def right_bottom_circle(self):
        img6 = self.threshold[1326:1414, 948:1034]
        #cv2.imshow("ff12", img6)
        self.nonzero16 = cv2.countNonZero(img6)
        #print("No of non zero in image16", self.nonzero16)
        cv2.imwrite('./leftjy/top/right1/top_bottom_circle.bmp', img6)


class cmpr:
     def compare(self):
          list = [pp.nonzero1, pp2.nonzero2, pp3.nonzero3, pp4.nonzero4, pp5.nonzero5, pp6.nonzero6]
          list3 = [3500, 1200, 2100, 5500, 1300, 3000]
          for i in range(0,6):
              if(list[i]>list3[i]):
                  print("Empy part")
              else:
                  print("Not Empty")
#          list2 = [pa.nonzero11, pa2.nonzero12, pa3.nonzero13, pa4.nonzero14, pa5.nonzero15,pa6.nonzero16]
#          print("first", list[0])
#          if list[0] > list2[0] and list[1] > list2[1]:
#              print("Empty part")
#          else:
#              print("Not ok part")
          list3 = [3500, 1200, 2100, 5500, 1300, 3000 ]
pp = image()
pp.image_left_top()

pp2 = image()
pp2.top_left_circle()

pp3 = image()
pp3.bottom_left_circle()

pp4 = image()
pp4.top_right_0()

pp5 = image()
pp5.top_right_circle_0()

pp6 = image()
pp6.right_bottom_circle()

pa = image2()
pa.image_left_top()

pa2 = image2()
pa2.top_left_circle()

pa3 = image2()
pa3.bottom_left_circle()

pa4 = image2()
pa4.top_right_0()

pa5 = image2()
pa5.top_right_circle_0()

pa6 = image2()
pa6.right_bottom_circle()

cc = cmpr()
cc.compare()

cv2.waitKey(0)

