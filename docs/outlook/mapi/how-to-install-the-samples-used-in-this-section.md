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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы установить приложение MFCMAPI и проект CreateOutlookItemsAddin для просмотра и запуска примера кода, на который ссылается раздел в разделе "Создание элементов Outlook с помощью [MAPI",](creating-outlook-items-by-using-mapi.md) выполните следующие действия. 

Чтобы скачать и установить примеры, используемые в разделе "Использование MAPI для создания элементов Outlook", выполните следующие действия.

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>Загрузка и установка приложения MFCMAPI и открытие проекта CreateOutlookItemsAddin

1. Скачайте текущую версию [исполняемого MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) в папку в системе. 
    
2. Извлекать MFCMapi.exe в MFCMapi.exe. _zip_ версии в пустую папку на жестком диске.
    
3. Скачайте текущую версию проекта [CreateOutlookItemsAddin.](https://go.microsoft.com/fwlink/?LinkID=127828) 
    
4. Извлекаете все файлы из CreateOutlookItemsAddin.zip в папку, в которой вы извлекли MFCMapi.exe на шаге 2.
    
5. Скопируйте MFCMapi.exe из папки, используемой на шаге 2, в каталог сборки для проекта CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).
    
6. Откройте проект CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) в Visual Studio, чтобы изучить исходный код. Чтобы определить, какие исходные файлы необходимо открыть, обратитесь к темам раздела "Создание элементов Outlook с помощью [MAPI".](creating-outlook-items-by-using-mapi.md) 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>Запуск MFCMAPI и проекта CreateOutlookItemsAddin

В следующих шагах предполагается, что вы загрузили и установили текущую версию исполняемого MFCMAPI и проекта CreateOutlookItemsAddin, как описано в предыдущей процедуре. Эти действия позволят вам пунктов меню **Addins,** которые позволяют создавать элементы Outlook с помощью приложения MFCMAPI и проекта CreateOutlookItemsAddin. 
  
> [!NOTE]
> Папка, выбранная на шаге 8, и команда, выбранная на шаге 9, зависит от типа элемента, рассмотренного в одном из разделов раздела "Создание элементов Outlook с помощью [MAPI".](creating-outlook-items-by-using-mapi.md) 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>Запуск команд приложения MFCMAPI и меню addins

1. Запустите Mfcmapi.exe папку CreateOutlookItemsAddin\Debug, которая создается при соответствии с инструкциями по установке.
    
2. Нажмите **кнопку "ОК",** чтобы отклонять экран-заставку MFCMAPI. 
    
3. В меню **"Сеанс"** щелкните **"Логон" и "Таблица магазина отображения".**
    
4. В **диалоговом** окне "Выбор профиля" выберите правильный профиль и нажмите кнопку **"ОК".** 
    
5. Дважды **щелкните "Почтовый ящик - _[Имя пользователя] в_** представлении списка таблицы магазина". 
    
6. В представлении дерева папок разоберем корневой узел. Имя корневого узла зависит от выбранного типа профиля. Обычно этот узел отображается в качестве **корневого почтового ящика.**
    
7. В представлении дерева папок разоберем узел, содержащий хранилище данных. Имя, отображаемая для этого узла, зависит от выбранного типа профиля. Обычно этот узел отображается в IPM_SUBTREE **или** **в верхней части информационного магазина.**
    
8. Дважды щелкните папку для создаваемого типа элемента. Например, чтобы создать встречу,  щелкните папку "Встречи". 
    
9. В меню **"Надстройки"** щелкните соответствующую команду для создаемой позиции. 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>Загрузка и просмотр кода из приложения MFCMAPI

Некоторые разделы относятся к коду из самого приложения MFCMAPI. Ниже описано, как скачать исходный код MFCMAPI и просмотреть его в Visual Studio. 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>Скачать и просмотреть исходный код приложения MFCMAPI

1. Загрузите исходный код для текущей версии [приложения MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) в папку в системе. 
    
2. Извлеките файлы в _zip-файле_ MFCMAPI в пустую папку на жестком диске.
    
3. Откройте проект MFCMapi (\ _foldername_\ MFCMapi.vcproj) в Visual Studio, чтобы изучить исходный код.
    
## <a name="see-also"></a>См. также

- [Создание простого почтового элемента](how-to-create-a-simple-mail-item.md)
- [Создание простого элемента повторяющейся задачи](how-to-create-a-simple-recurrent-task-item.md)
- [Создание сложного элемента повторяющейся встречи](how-to-create-a-complex-recurrent-appointment-item.md)
- [Чтение и разбиение шаблона повторения](how-to-read-and-parse-a-recurrence-pattern.md)

