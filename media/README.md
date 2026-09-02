# Папка для медиа-файлов (фото и видео)

Положите сюда ваши файлы:

- **Фото:** photo1.jpg, photo2.jpg и т.д. (форматы: JPG, PNG, WEBP)
- **Видео:** video1.mp4, video2.mp4 и т.д. (формат: MP4)

## Примеры:
```
media/
├── photo1.jpg
├── photo2.jpg
├── photo3.png
└── ceremony.mp4
```

## В коде:

Раскомментируйте строки в функции `загрузитьМедиа()` в файле `index.html`:

```javascript
const файлы = [
    { тип: 'фото', путь: 'media/photo1.jpg' },
    { тип: 'фото', путь: 'media/photo2.jpg' },
    { тип: 'видео', путь: 'media/video1.mp4' }
];

файлы.forEach(файл => {
    const элемент = document.createElement('div');
    элемент.className = 'галерея__элемент';
    
    if (файл.тип === 'фото') {
        элемент.innerHTML = `<img src="${файл.путь}" alt="Фото" loading="lazy">`;
    } else if (файл.тип === 'видео') {
        элемент.innerHTML = `<video controls><source src="${файл.путь}"></video>`;
    }
    
    галерея.appendChild(элемент);
});
```

После этого фото и видео автоматически загрузятся на сайт!
