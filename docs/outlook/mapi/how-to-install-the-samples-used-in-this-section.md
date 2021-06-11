---
title: Установка примеров, используемых в этом разделе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345551"
---
# <a name="install-the-samples-used-in-this-section"></a>Установка примеров, используемых в этом разделе

**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы установить приложение MFCMAPI и проект CreateOutlookItemsAddin для просмотра и запуска примера кода, на который ссылается тема в разделе Создание элементов Outlook с помощью [mapi,](creating-outlook-items-by-using-mapi.md) выполните следующие действия. 

Чтобы скачать и установить примеры, используемые в разделе "Использование MAPI для создания элементов Outlook", выполните следующие действия.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Загрузка и установка приложения MFCMAPI и открытие проекта CreateOutlookItemsAddin

1. Скачайте текущую версию [MFCMAPI,](https://go.microsoft.com/fwlink/?LinkID=124154) исполняемую в папку в вашей системе. 
    
2. Извлечение MFCMapi.exe в MFCMapi.exe. _версия_.zip в пустую папку на жестком диске.
    
3. Скачайте текущую версию [проекта CreateOutlookItemsAddin.](https://go.microsoft.com/fwlink/?LinkID=127828) 
    
4. Извлекать все файлы в CreateOutlookItemsAddin.zip в папку, в которой был извлечен MFCMapi.exe в шаге 2.
    
5. Скопируйте MFCMapi.exe из папки, используемой в шаге 2, в каталог сборки для проекта CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Откройте проект CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) в Visual Studio изучить исходный код. Обратитесь к темам из раздела Создание элементов Outlook с помощью [раздела MAPI,](creating-outlook-items-by-using-mapi.md) чтобы определить, какие исходные файлы открыть. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Запуск MFCMAPI и проекта CreateOutlookItemsAddin

Следующие действия предполагают, что вы скачали и установили текущую версию исполняемого MFCMAPI и проекта CreateOutlookItemsAddin, как описано в предыдущей процедуре. В этих действиях вы сможете найти элементы меню **Addins,** которые позволяют создавать элементы Outlook с помощью приложения MFCMAPI и проекта CreateOutlookItemsAddin. 
  
> [!NOTE]
> Папка, выбранная на шаге 8, и команда, выбранная на шаге 9, зависит от типа элемента, рассмотренного в одной из тем из раздела Создание элементов Outlook с помощью [раздела MAPI.](creating-outlook-items-by-using-mapi.md) 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Запуск команд приложения MFCMAPI и меню Addins

1. Начните Mfcmapi.exe в папке CreateOutlookItemsAddin\Debug, которая создается при соответствии инструкциям по установке.
    
2. Нажмите **кнопку ОК,** чтобы отклонять экран всплеска MFCMAPI. 
    
3. В меню **Сеанс** нажмите **кнопку Logon и Display Store Table**.
    
4. В **диалоговом** окне Выберите профиль выберите правильный профиль и нажмите **кнопку ОК.** 
    
5. Дважды **щелкните почтовый ящик _[Имя пользователя]_** в представлении списка таблицы хранения. 
    
6. В представлении дерева папки разложите корневой узел. Имя, отображаемого для корневого узла, зависит от выбранного типа профиля. Обычно этот узел отображается как **Root - Почтовый ящик.**
    
7. В представлении дерева папки разложите узел, содержащий хранилище сведений. Имя, отображаемого для этого узла, зависит от выбранного типа профиля. Обычно этот узел отображается  в IPM_SUBTREE **или в верхней части магазина информации.**
    
8. Дважды щелкните папку для создания типа элемента. Например, чтобы создать встречу, щелкните папку **"Встречи".** 
    
9. В меню **Addins** щелкните соответствующую команду для создания элемента. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Скачивание и просмотр кода из приложения MFCMAPI

Некоторые темы ссылаются на исходный код из самого приложения MFCMAPI. Ниже описано, как скачать исходный код MFCMAPI и просмотреть его в Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Загрузка и просмотр исходный код приложения MFCMAPI

1. Скачайте исходный код текущей версии [приложения MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) в папку в вашей системе. 
    
2. Извлечение файлов в папке MFCMAPI-changeset.zip пустой папке на жестком диске. 
    
3. Откройте проект MFCMapi _(\foldername_\ MFCMapi.vcproj) в Visual Studio, чтобы изучить исходный код.
    
## <a name="see-also"></a>См. также

- [Создание элемента простой почты](how-to-create-a-simple-mail-item.md)
- [Создание элемента простой повторяющейся задачи](how-to-create-a-simple-recurrent-task-item.md)
- [Создание сложного элемента периодических встреч](how-to-create-a-complex-recurrent-appointment-item.md)
- [Read and Parse a Recurrence Pattern](how-to-read-and-parse-a-recurrence-pattern.md)

