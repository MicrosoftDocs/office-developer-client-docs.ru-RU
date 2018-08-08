---
title: Установка примеров, используемые в данном разделе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4c5b6cbdda63dcb79b23253e0db695ae658c4fa4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808620"
---
# <a name="install-the-samples-used-in-this-section"></a>Установка примеров, используемые в данном разделе

**Относится к**: Outlook 
  
Чтобы установить приложение mfcmapi (en) и CreateOutlookItemsAddin проекта для просмотра и запустите пример кода, ссылок на них в разделе [Создание элементов Outlook с помощью интерфейса MAPI](creating-outlook-items-by-using-mapi.md) , выполните следующие действия. 

Чтобы загрузить и установить примеры, используемые в «с помощью интерфейса MAPI для создания элементов Outlook» раздела, выполните следующие действия.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Чтобы загрузить и установить приложение mfcmapi (en) и откройте проект CreateOutlookItemsAddin

1. Загрузите текущую версию [mfcmapi (en)](http://go.microsoft.com/fwlink/?LinkID=124154) исполняемый файл в папку на компьютере. 
    
2. Извлеките файл MFCMapi.exe в MFCMapi.exe. _версия_.zip в пустую папку на жестком диске.
    
3. Загрузите текущую версию [CreateOutlookItemsAddin](http://go.microsoft.com/fwlink/?LinkID=127828) project. 
    
4. Извлечь все файлы в файле CreateOutlookItemsAddin.zip к папке, куда были извлечены файл MFCMapi.exe в шаге 2.
    
5. Скопируйте MFCMapi.exe из папки, используемые в шаге 2 папке построения проекта CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Откройте проект CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) в Visual Studio, чтобы просмотреть исходный код. Ссылки на разделы, из раздела [Создание элементов Outlook с помощью интерфейса MAPI](creating-outlook-items-by-using-mapi.md) , чтобы определить, какие исходные файлы для открытия. 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Запустите проект CreateOutlookItemsAddin и mfcmapi (en)

Предполагается, что вы загрузили и установили текущая версия исполняемый файл mfcmapi (en) и CreateOutlookItemsAddin проект, как описано в предыдущей процедуре. Эти шаги позволят к пунктам меню **Addins** для создания элементов Outlook с помощью приложения mfcmapi (en) и CreateOutlookItemsAddin проекта. 
  
> [!NOTE]
> Папка, выбранного в шаге 8 и команды, выбранного в шаге 9, зависит от типа элемента, обсуждаемые в одном из разделов из раздела [Создание элементов Outlook с помощью интерфейса MAPI](creating-outlook-items-by-using-mapi.md) . 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Для запуска приложения mfcmapi (en) и команды меню Addins

1. Запустите Mfcmapi.exe в папке CreateOutlookItemsAddin\Debug, созданный при следуйте инструкциям по установке.
    
2. Нажмите **кнопку ОК** , чтобы закрыть экран-заставка mfcmapi (en). 
    
3. В меню **сеанса** выберите команду **Вход в систему и отображения хранилища в таблице**.
    
4. В диалоговом окне **Выбор профиля** выберите правильный профиль и нажмите кнопку **ОК**. 
    
5. Дважды щелкните значок **почтовый ящик - _[Имя пользователя]_ ** в представлении списка в таблице хранилища. 
    
6. В древовидном представлении папки разверните корневой узел. Имя, отображаемое для корневого узла, может изменяться в зависимости от типа выбранного профиля. Обычно этот узел отображается как **корень - почтового ящика**.
    
7. В древовидном представлении папки разверните узел, содержащий банка данных. Имя, отображаемое для этого узла, может изменяться в зависимости от типа выбранного профиля. Обычно этот узел отображается в виде **IPM_SUBTREE** или **Хранилища**.
    
8. Дважды щелкните папку с типом элемента для создания. Например для создания встречи, щелкните папку **встреч** . 
    
9. В меню " **надстройки** " выберите соответствующую команду для элемента для создания. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Загрузка и просмотр кода из приложения mfcmapi (en)

Некоторые разделы ссылаться на исходный код из самого приложения mfcmapi (en). Ниже описывается загрузка mfcmapi (en) исходного кода и просмотр в Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Чтобы загрузить и просмотреть исходный код приложения mfcmapi (en)

1. Загрузите исходный код для текущей версии приложения [mfcmapi (en)](http://go.microsoft.com/fwlink/?LinkID=124154) в папку на компьютере. 
    
2. Извлеките файлы в .zip _изменений_mfcmapi (en) — чтобы очистить папку на жестком диске.
    
3. Откройте проект mfcmapi (en) (\ _foldername_\ MFCMapi.vcproj) в Visual Studio для просмотра исходного кода.
    
## <a name="see-also"></a>См. также

- [Создание простого почтового элемента](how-to-create-a-simple-mail-item.md)
- [Создание простого элемента повторяющейся задачи](how-to-create-a-simple-recurrent-task-item.md)
- [Создание сложного элемента повторяющейся встречи](how-to-create-a-complex-recurrent-appointment-item.md)
- [Чтение и анализ расписания повторения](how-to-read-and-parse-a-recurrence-pattern.md)

