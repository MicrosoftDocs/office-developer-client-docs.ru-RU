---
title: Поддержка Office для Android для платформы Android Storage Access Framework
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office для Android интегрируется с платформой Android Storage Access Framework, которая позволяет Office открывать файлы, хранимые другим поставщиком документов.
ms.openlocfilehash: 24d7e48106aeb5e58a668b94cbde00eaa9175230
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300352"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a>Поддержка Office для Android для платформы Android Storage Access Framework

Office для Android интегрируется с платформой Android Storage Access Framework, которая позволяет Office открывать файлы, хранимые другим поставщиком документов.
  
Android 4.4 (API уровня 19) представляет платформу Storage Access Framework (SAF). SAF позволяет пользователям просматривать и открывать документы, изображения и другие файлы всех поставщиков хранилищ документов, которые предпочитают пользователи. Стандартный пользовательский интерфейс позволяет просматривать файлы и получать доступ к ним подходящим способом по всем приложениям и поставщикам.
  
## <a name="implement-a-document-provider"></a>Реализация поставщика документа

Если вы разрабатываете приложение, предоставляющее службы хранения для документов, вы можете предоставить доступ к файлам через платформу SAF, [записав поставщика пользовательских документов](https://developer.android.com/guide/topics/providers/document-provider.html). Затем приложения Office могут вызвать намерение [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) и/или [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html). чтобы получить файлы, возвращенные поставщиком документов. Обратите внимание, что намерение может включать фильтры для дальнейшего уточнения критериев. 
  
## <a name="enable-free-consumer-edits"></a>Включение бесплатных правок для пользователей

Пользователи могут входить в приложения Office с помощью бесплатной учетной записи Майкрософт, чтобы создавать или редактировать документы, хранящиеся в службе хранения, ориентированной на пользователя. В следующей таблице перечислены обязательные свойства, которые поставщики обязаны поставлять как часть курсора, чтобы позволить пользователям бесплатно редактировать документы, доступные через платформу Storage Access Framework.
  
|**Свойство**|**Индекс**|**Значение**|
|:-----|:-----|:-----|
|Тип документа  <br/> |com_microsoft_office_doctype  <br/> |\<consumer\>  <br/> |
|Понятное имя службы  <br/> |com_microsoft_office_servicename  <br/> |Любое понятное для пользователей имя службы, используемое для определения документа в списке недавно использовавшихся документов в приложениях Office. Обратите внимание, что свойство "Условия соглашения" должно быть предоставлено до того, как будет отображено понятное имя службы.  <br/> |
|Условия соглашения  <br/> |com_microsoft_office_termsofuse  <br/> |\<Я соглашаюсь с условиями, указанными на странице https://go.microsoft.com/fwlink/p/?LinkId=528381\>  <br/> |
   
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Интеграция с Office](integrate-with-office.md)
    
- [Основные сведения о поставщике содержимого](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [Создание поставщика содержимого](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [Руководство разработчика Storage Access Framework](https://developer.android.com/guide/topics/providers/document-provider.html)
    

