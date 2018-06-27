---
title: Кэш псевдонимов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Последнее изменение: 30 января 2013 г.'
ms.openlocfilehash: 1ea1d3e6f636cf6a3ad47b6fdfe88d0f7130a5f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810038"
---
# <a name="nickname-cache"></a>Кэш псевдонимов

 
  
**Применимо к**: Outlook 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 и Microsoft Outlook 2013 взаимодействовать с кэш псевдонимов, также известной как «Автозаполнение поток.» Поток автозаполнения магазина Outlook остается в списке автозаполнения — список имен, которое отображает в **к**, **Cc**, и **Bcc** редактировать поля, когда пользователь создает сообщение электронной почты. В этом разделе описываются взаимодействия Outlook 2007, Outlook 2010 и Outlook 2013 с потоком автозаполнения и также двоичный формат файла и рекомендуемые способы взаимодействия с потока автозаполнения. 
  
Для приложений, которые взаимодействуют с Outlook 2010 или Outlook 2013 в потоке автозаполнения сохраняется как свойство MAPI и могут изменяться с помощью протокола MAPI или объект **PropertyAccessor** сообщения. Объект **PropertyAccessor** , открытой в объектной модели Outlook 2010 или Outlook 2013. 
  
Существуют зависимости, объектную модель Outlook 2007 или API MAPI. Таким образом приложения, вносить изменения в потоке автозавершения в Outlook 2007 можно записать с помощью любого языка программирования.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Взаимодействие с потоком автозаполнения

При доступе к поля ввода **, **копия**или **Скрытая копия** **сообщения, загружены в потоке автозаполнения и отображается список имен пользователей. Outlook взаимодействует с потоком автозаполнения двумя способами: 
  
1. Загрузка потока автозаполнения 
    
2. Сохранение изменений в данные в потоке автозаполнения
    
Средства хранения данных автозаполнения отличается в Outlook 2007 и Outlook 2010 или Outlook 2013 следующим образом: 
  
 **Outlook 2007**
  
Для Outlook 2007 в потоке автозаполнения хранятся в файле с тем же именем, как профиль и расширение .nk2. Например, при использовании профилем по умолчанию «outlook» файл будет называться «outlook.nk2». Файл .nk2 сохраняется в папке % APPDATA%\Microsoft\Outlook. Дополнительные сведения о формате двоичных файлов кэш псевдонимов содержатся в разделе [Формат файла Outlook 2003 и 2007 NK2 и рекомендации для разработчиков](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 и Outlook 2013**
  
Outlook 2010 или Outlook 2013 считывает поток автозаполнения из сообщения в таблице связанного содержимого папки "Входящие" хранилища доставки учетной записи электронной почты. В этом скрытого сообщения имеет класс сообщения и темы IPM. Configuration.Autocomplete. Поток автозаполнения хранятся на это сообщение в свойстве PR_ROAMING_BINARYSTREAM ([Каноническое свойство PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)). Автозаполнение данных может временно кэшируются в dat Автозаполнение-файл находится в папке % USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. Тем не менее DAT-файл — только кэш и не используется для обратной записи в хранилище доставки при выходе пользователя из Outlook 2010 или Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Загрузка потока автозаполнения

Outlook загружает поток автозаполнения при инициализации элемента с адресации функциональными возможностями. Например адреса электронной почты используются в новых сообщений, ответ почты, элемента контакта, приглашения на собрание и т. д. Для загрузки данных Outlook считывает все содержимое потока в памяти.
  
Для операций автозаполнения Outlook взаимодействует только с эту структуру в памяти во время существования процесса outlook.exe. Структура сохраняет Outlook только при завершении работы. В следующем разделе «Сохранение потока автозаполнение» для получения дополнительных сведений по этому процессу.
  
## <a name="saving-the-autocomplete-stream"></a>Сохранение в потоке автозаполнения

Поток автозаполнения сохраняет Outlook при завершении работы при изменении списка автозавершения в любом из следующих способов:
  
- Сопоставления имен, комплектации получателя в диалоговом окне адресной книги или отправка почты получателя, который уже отсутствует в списке Добавить новый элемент псевдонимов.
    
- Запись изменяется путем отправки почты для существующего получателя в списке.
    
- Запись было удалено пользователем с помощью пользовательского интерфейса.
    
- Другие вспомогательные сценарии, не относящиеся к этому разделу.
    
Сохранение изменений в данные автозаполнения включает в себя обратной записи структуры в памяти в [поток автозаполнения](autocomplete-stream.md). При взаимодействии с Outlook 2007 поток сохраняется в локальном .nk2 файл. Для Outlook 2010 или Outlook 2013 в потоке автозаполнения записывает обратно в таблице связанное содержимое из папки "Входящие" хранилища доставки учетной записи электронной почты.
  
## <a name="recommendations"></a>Рекомендации

- Изменение никогда не частично потока автозаполнения. Поддерживаемые взаимодействия — (1) чтение потока всей автозавершения в память, (2) изменения структуры памяти и (3) всей потока обратной записи на любой таблице связанное содержимое из папки "Входящие" хранилища доставки учетной записи электронной почты (для Outlook 2010 или Outlook 2013) или к файлу локального .nk2 (Outlook 2007).
    
- Не взаимодействуют с потока автозаполнения запущенном приложении Outlook. Если Outlook выполняется во время изменения потока, скорее всего перезапишет изменения, когда завершает работу.
    
- Не свойства записи введите PT_MV_UNICODE и PR_MV_STRING8 в поток автозаполнения для работы с ними в Microsoft Outlook 2003. Эти свойства только понятны Outlook 2007, Outlook 2010 и Outlook 2013.
    
- При разработке кода, который взаимодействует с Outlook 2007, рекомендуется заблокировать файл .nk2 от изменения другими процессами, во время чтение и запись с помощью стандартных блокировки API-интерфейсы (например, **LockFile** в C/C++ и **файла FileStream.Lock** в C#). 
    
- Только изменения свойств типов, которые являются из набора строк в потоке автозаполнения. Дополнительные сведения о свойствах потока автозаполнения и типы свойств можно [автозаполнения потока](autocomplete-stream.md).
    
## <a name="see-also"></a>См. также



[Поток автозаполнения](autocomplete-stream.md)
  
[Профили MAPI](mapi-profiles.md)


[Формат файлов Outlook 2003 и 2007 NK2 и рекомендации для разработчиков](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
