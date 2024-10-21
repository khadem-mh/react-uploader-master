<img src="https://github.com/khadem-mh/pictures/blob/khadem/2024-10-16_14-52-38.png?raw=true" width="1000">

# A quick look

- __**Help your website's UX with this package**__

- A package for previewing the photo selected by the user with the possibility of deleting the previous image and uploading a new one

- After selecting the image desired by the user, the complete information of this image will be sent to you through the onDataSend property

- Ability to change text, color, shadow, etc. in Uploader

- The user can only upload a valid image with the format (of your choice).

- Ability to receive GIF from the user and preview it

- Ability to set the desired width and height to Uploader

## Upload Image In Package
<p align="center">
<img src="https://github.com/khadem-mh/pictures/blob/khadem/uploader.gif?raw=true" width="500">
</p>

## Error Handling In Package
<p align="center">
  <img src="https://github.com/khadem-mh/pictures/blob/khadem/uploader-err.gif?raw=true" width="500">
</p>

## *Next Release * Adding the ability to drag and drop the image in the Uploader box 👨‍💻*

## Usage ✍
- Install Package
```bash
npm i react-uploader-master
```
- Import the Uploader component first.
```javascript
import Uploader from 'react-uploader-master'
```
- Then enter these essential items to launch Uploader
```javascript
<Uploader
  onDataSend={file => {
    setFile(file) // Necessary
  }}
/>
```

# Ready Example
```javascript
import { useState, useEffect } from 'react';
import Uploader from 'react-uploader-master'

export default function App() {
  const [file, setFile] = useState(null)

  useEffect(() => {
    if (file) {
      console.log(file);
    }
  }, [file])

  return (
    <div>

      <Uploader
        onDataSend={file => {
          setFile(file) // Necessary
        }}
        // ↓ by default set
        //imgFormatsAllow={['jpg', 'jpeg', 'png', 'webp', 'jfif']}
        //imgFormatsNotAllowed={['tiff', 'bmp', 'svg', 'gif']}
      />

    </div>
  );
}
```

## Package Props 👨‍💻
| Parameter               | Type       | Field Status    | Description              |
| :--------               | :-------   | :------         | :-------------------------------- |
| `boxWidth`              | `Number`   | **_Optional_**  | Setting the width for the uploader box |
| `boxHeight`             | `Number`   | **_Optional_**  | Setting the height for the uploader box |
| `bgColor`               | `String`   | **_Optional_**  | Setting the background color for the Uploader box |
| `boxShadow`             | `Boolean`  | **_Optional_**  | Enable or disable shadow behind Uploader |
| `minSizeImg`            | `Number`   | **_Optional_**  | Specifies the minimum size of a photo (the number you enter is in kilobytes) |
| `maxSizeImg`            | `Number`   | **_Optional_**  | Specifies the maximum size of a photo (the number you enter is in kilobytes) |
| `activeRemoveBtn`       | `Boolean`  | **_Optional_**  | The delete button enables or disables the photo selected by the user |
| `displayModeRemoveBtn`  | `String`   | **_Optional_**  | you can change the delete button to 'icon' or 'btn'. |
| `imgFormatsAllow`       | `Array`    | **_Optional_**  | Valid formats for the photos you accept |
| `imgFormatsNotAllowed`  | `Array`    | **_Optional_**  | Invalid formats for photos you don't accept |
| `title`                 | `String`   | **_Optional_**  | You can replace the text in the Uploader box with your desired text |
| `onDataSend`            | `Function` | **_Required_**  | To access the information of the user's selected photo, it returns a function containing an argument named file |

### ╔╚ `onDataSend` ╝╗

`onDataSend` To access the information of the user's selected photo, it returns a function containing an argument named file

| Parameter    | Type       | Field Status    | Description              |
| :--------    | :-------   | :------         | :-------------------------------- |
| `file`       | `Array`    | **_Required_**  | It contains complete information about the image selected by the user |

How to use and get the file argument from the function input:

```javascript
onDataSend={file => {
    setFile(file)  // Necessary
}}
```
___
<img src="https://github.com/khadem-mh/khadem-mh/blob/khadem/my-img/2024-10-01_17-25-38.png" width="1000"/>

>### Social Network
> [<img src="https://github.com/khadem-mh/pagination-react/blob/main/public/Images/github.png" width="30">](https://github.com/khadem-mh)
> [<img src="https://github.com/khadem-mh/pagination-react/blob/main/public/Images/linkedin.png" width="30">](https://www.linkedin.com/in/khadem-mh/)
> [<img src="https://github.com/khadem-mh/pagination-react/blob/main/public/Images/telegram.png" width="30">](https://t.me/mhkhadem)
