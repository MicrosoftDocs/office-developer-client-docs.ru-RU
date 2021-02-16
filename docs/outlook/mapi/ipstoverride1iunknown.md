---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315500"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет поставщику файлов личных папок (PST) переопределять политику PSTDisableGrow.
  
|||
|:-----|:-----|
|Наследуется от:  <br/> |IUnknown  <br/> |
|Реализовано в:  <br/> |Поставщик PST-магазина  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Извлекает список регистраций для файла личных папок (PST).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Регистрирует файлы личных папок для автоматической разблокировки, избегая дальнейших вызовов hrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Разблокирует файл личных папок для роста.  <br/> |
   
## <a name="remarks"></a>Примечания

Идентификаторы интерфейса обработчиков переопределения PST-файлов могут быть не определены в загружаемом файле заголовщика, который вы найдете в разделе "Константы [MAPI"](mapi-constants.md) и сможете копировать и добавлять их в код. Используйте макрос DEFINE_GUID, определенный в файле guiddef.h файла загона SDK, чтобы связать символьные имена глобального уникального идентификатора (GUID) с их значениями. 
  
Дополнительные сведения см. в реализации обработора переопределения PST-данных для обхода [политики PSTDisableGrow в Outlook 2007.](https://support.microsoft.com/kb/956070)
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

