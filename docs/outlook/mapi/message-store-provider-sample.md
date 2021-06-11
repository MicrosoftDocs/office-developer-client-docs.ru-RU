---
title: Пример поставщика магазина сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436869"
---
# <a name="message-store-provider-sample"></a>Пример поставщика магазина сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщик личных папок (PST) в качестве заднего конца для хранения данных использует поставщика файлов персональных папок ( PST). Поставщик магазина PST, завернутый в пакет, должен использоваться вместе с API репликации. 
  
API репликации позволяет реплицировать элементы из заднего хранилища данных в хранилище Outlook PST. API репликации используется для репликации данных в специальный хранилище PST и отслеживания состояния синхронизации. Дополнительные сведения см. [в aPI репликации.](about-the-replication-api.md)
  
Большинство функций в поставщике магазина PST с пакетом образца передают свои аргументы непосредственно основному поставщику PST. Некоторые функции требуют особой реализации и описаны в следующих темах.
  
|||
|:-----|:-----|
|Исполняемый:  <br/> |WrpPST32.dll  <br/> |
|Каталог исходных кодов:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Язык:  <br/> |C++  <br/> |
|Платформы:  <br/> |Microsoft Visual Studio 2008 для Windows Vista, Windows Server 2008, Windows XP SP2 и Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Поддерживаемые функции

Этот пример поддерживает Microsoft Outlook 2010, русская версия 64-битный и в настоящее время пересмотрен для Outlook 2013 г. Дополнительные сведения см. в следующих разделах:
  
- [Сведения об API репликации](about-the-replication-api.md)
    
- [Инициализация поставщика упакованных магазинов PST](initializing-a-wrapped-pst-store-provider.md)
    
- [Ведение журнала в поставщике упакованных магазинов PST](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Использование поставщика упакованных магазинов PST](using-a-wrapped-pst-store-provider.md)
    
- [Отключение поставщика упакованных магазинов PST](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Установка поставщика магазинов PST Sample Wrapped**
  
1. Чтобы скачать поставщик пакетов PST sample, см. в примере Загрузка Outlook [MAPI Samples](downloading-the-outlook-mapi-samples.md).
    
2. Найдите папку, в которой сохранены Outlook MAPI Samples. Щелкните правой кнопкой **мыши папку OutlookMAPISamples-version \< \> number** zip и нажмите кнопку **Извлечь все**.
    
3. Щелкните **Обзор,** выберите расположение, в котором необходимо сохранить образец, а затем нажмите кнопку **Извлечение**.
    
4. Запуск Microsoft Visual Studio 2008 г.
    
5. В Microsoft Visual Studio 2008 нажмите **кнопку Файл**, выберите **Открыть**, а затем **нажмите кнопку Project/Решение**.
    
6. Просмотрите расположение, в котором сохранен пример, щелкните **WrapPST.vcproj** и нажмите **кнопку Открыть**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. В **диалоговом окне Сохранить файл как** диалоговое окно нажмите **кнопку Сохранить**.
    
9. В папке, в которой сохранен пример,  щелкните правой кнопкой мыши файлinstall.batи нажмите **кнопку Выполнить в качестве администратора**.
    
10. В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.
    

