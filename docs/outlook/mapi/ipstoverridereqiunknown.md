---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356982"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Доступ к ресурсам поставщика файлов личных папок (PST).
  
|||
|:-----|:-----|
|Наследуется от:  <br/> |IUnknown  <br/> |
|Реализовано в:  <br/> |Поставщик PST-магазина  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Инициирует процедуру разблокировки для файла личных папок (PST).  <br/> |
   
## <a name="remarks"></a>Примечания

Идентификаторы интерфейса обработчиков переопределения PST-файлов могут быть не определены в загружаемом файле заголовщика, который вы найдете в разделе "Константы [MAPI"](mapi-constants.md) и сможете копировать и добавлять их в код. Используйте макрос DEFINE_GUID, определенный в файле guiddef.h файла загона SDK, чтобы связать символьные имена глобального уникального идентификатора (GUID) с их значениями. 
  
Дополнительные сведения см. в реализации обработора переопределения PST-данных для обхода [политики PSTDisableGrow в Outlook 2007.](https://support.microsoft.com/kb/956070)
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

