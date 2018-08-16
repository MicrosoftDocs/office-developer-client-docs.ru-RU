---
title: Пример поставщика хранилища сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b3c907b0a53a41a52516b23ffb1cf7400d887d89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810014"
---
# <a name="message-store-provider-sample"></a>Пример поставщика хранилища сообщений

  
  
**Относится к**: Outlook 
  
Оболочку PST поставщик хранилища использует поставщика личных папок (PST) файла как серверные компоненты для хранения данных. Оболочку поставщика хранилища PST-файлов можно использовать интерфейс API репликации. 
  
API репликации можно реплицировать элементов из хранилища данных в Microsoft Outlook PST-хранилище. Использование API репликации для репликации данных в выделенном PST-хранилище и отслеживание состояния синхронизации. Дополнительные сведения [О репликации API](about-the-replication-api.md)см.
  
Большая часть функций в оболочку PST поставщик хранилища передать свои аргументы непосредственно к базовым поставщиком PST-файлов. Некоторые функции требуют специальных реализаций и описаны в следующих разделах.
  
|||
|:-----|:-----|
|Исполняемый файл:  <br/> |WrpPST32.dll  <br/> |
|Каталог исходного кода:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Язык:  <br/> |C++  <br/> |
|Платформы:  <br/> |Microsoft Visual Studio 2008 для компиляции для Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1  <br/> |
   
## <a name="supported-features"></a>Поддерживаемые функции

В этом примере поддерживает Microsoft Outlook 2010, 64-разрядная версия и теперь обновлен для Outlook 2013. В следующих разделах для получения дополнительных сведений:
  
- [Сведения об API репликации](about-the-replication-api.md)
    
- [Инициализация поставщика упакованного PST-хранилища](initializing-a-wrapped-pst-store-provider.md)
    
- [Вход в систему поставщика упакованного PST-хранилища](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Использование поставщика упакованного PST-хранилища](using-a-wrapped-pst-store-provider.md)
    
- [Завершение работы поставщика упакованного PST-хранилища](shutting-down-a-wrapped-pst-store-provider.md)
    
 **Чтобы установить оболочку PST поставщик хранилища**
  
1. Чтобы загрузить поставщик оболочку PST-файлов, обратитесь к разделу [Загрузка примеров Outlook MAPI](downloading-the-outlook-mapi-samples.md).
    
2. Найдите папку, в которой вы сохранили примеры Outlook MAPI. Щелкните правой кнопкой мыши **OutlookMAPISamples -\<номер версии\> ** ZIP-папку и выберите команду **Извлечь все**.
    
3. Нажмите кнопку **Обзор**, выберите расположение, где требуется сохранить образца и нажмите кнопку **извлечь**.
    
4. Запустите Microsoft Visual Studio 2008.
    
5. В Microsoft Visual Studio 2008 откройте меню **файл**, выберите команду **Открыть**и выберите **Проект/решение**.
    
6. Перейдите к папке, в которой вы сохранили примера **WrapPST.vcproj**и нажмите кнопку **Открыть**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. В диалоговом окне **Сохранение файла** нажмите кнопку **Сохранить**.
    
9. В папке, где был сохранен примера щелкните правой кнопкой мыши файл **install.bat** и выберите команду **Запуск от имени администратора**.
    
10. В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.
    
