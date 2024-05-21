echo "Building Script"

# create executable
python -m PyInstaller --onefile duplicates.py

# move the .exe to main folder
cd dist
mv duplicates.exe ../
cd ../

# remove stuff
echo "Removing stuff"
rm -rf ./build
rm -rf ./dist
rm duplicates.spec

# run the program
start duplicates.exe