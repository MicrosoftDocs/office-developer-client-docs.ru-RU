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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет поставщику файлов персональных папок (PST) переопределять политику PSTDisableGrow.
  
|||
|:-----|:-----|
|Наследует от:  <br/> |IUnknown  <br/> |
|Реализовано в:  <br/> |Поставщик магазинов PST  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Извлекает список регистраций для файла "Личные папки" (PST).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Регистрирует файлы личных папок для автоматической разблокировки, избегая дополнительных вызовов в HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Открывает файл личных папок для роста.  <br/> |
   
## <a name="remarks"></a>Примечания

Идентификаторы интерфейса обработчиков обработчиков PST не могут быть определены в файле загружаемых заголовок, который вы сейчас имеете, и в этом случае вы найдете их в разделе [MAPI Constants](mapi-constants.md) и сможете скопировать и добавить их в код. Используйте макрос DEFINE_GUID, определенный в файле guiddef.h Windows набора разработки программного обеспечения (SDK), чтобы связать символические имена глобального уникального идентификатора (GUID) с их значениями. 
  
Дополнительные сведения см. в рубрике Как реализовать обработник переопределения PST для обхода политики [PSTDisableGrow в Outlook 2007 г.](https://support.microsoft.com/kb/956070)
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

