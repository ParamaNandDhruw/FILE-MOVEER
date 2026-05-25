#FILE MOVER

import os
import shutil

FOLDER_NAME = "image"

if not os.path.exists(FOLDER_NAME):
	os.mkdir(FOLDER_NAME)

FOLDER_NAME1 = "video"
if not os.path.exists(FOLDER_NAME1):
	os.mkdir(FOLDER_NAME1)
	
FOLDER_NAME2 = "files"	
if not os.path.exists(FOLDER_NAME2):
	os.mkdir(FOLDER_NAME2)
	
print("------- FILES ORGINYZER -------")
print("1) .txt for file\n2) .png for image\n3) .mp4 for video")

USER_CHOICE = input("Enter files name: ").lower()
FILES_TYPE = input("files type: ").lower()

if os.path.exists(USER_CHOICE) and FILES_TYPE == "1":
	FULL_PATH = os.path.join(FOLDER_NAME2, USER_CHOICE)
	shutil.move(USER_CHOICE, FOLDER_NAME2)
	print(FULL_PATH)

	
elif os.path.exists(USER_CHOICE) and FILES_TYPE == "2":
	FULL_PATH = os.path.join(FOLDER_NAME1, USER_CHOICE)
	shutil.move(USER_CHOICE, FOLDER_NAME1)
	print("done...")


	
elif os.path.exists(USER_CHOICE) and FILES_TYPE == "3":
	FULL_PATH = os.path.join(FOLDER_NAME, USER_CHOICE)
	shutil.move(USER_CHOICE, FOLDER_NAME)
	print(FULL_PATH)

else:
	print("files not found.....")