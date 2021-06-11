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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Доступ к ресурсам поставщика файлов личных папок (PST).
  
|||
|:-----|:-----|
|Наследует от:  <br/> |IUnknown  <br/> |
|Реализовано в:  <br/> |Поставщик магазинов PST  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Инициирует процедуру разблокировки для файла личных папок (PST).  <br/> |
   
## <a name="remarks"></a>Примечания

Идентификаторы интерфейса обработчиков обработчиков PST не могут быть определены в файле загружаемых заголовок, который вы сейчас имеете, и в этом случае вы найдете их в разделе [MAPI Constants](mapi-constants.md) и сможете скопировать и добавить их в код. Используйте макрос DEFINE_GUID, определенный в файле guiddef.h Windows набора разработки программного обеспечения (SDK), чтобы связать символические имена глобального уникального идентификатора (GUID) с их значениями. 
  
Дополнительные сведения см. в рубрике Как реализовать обработник переопределения PST для обхода политики [PSTDisableGrow в Outlook 2007 г.](https://support.microsoft.com/kb/956070)
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

