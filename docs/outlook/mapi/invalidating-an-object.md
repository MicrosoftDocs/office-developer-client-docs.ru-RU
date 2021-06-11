---
title: Недействительный объект
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407678"
---
# <a name="invalidating-an-object"></a>Недействительный объект

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В процессе остановки поставщика может потребоваться признать объект недействительным. Недействительный объект включает замену его vtable на vtable, который содержит реализации для трех **методов IUnknown:** **AddRef**, **Release** и **QueryInterface**. Недействительный объект, назвав [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), метод, включенный в объект поддержки каждого из трех типов общего поставщика. Поставщики обычно делают этот вызов в реализации метода Logoff своего объекта **logon.** 
  
Недействительный доступ к объекту предоставляет MAPI конечную ответственность за то, чтобы освободить память, связанную с объектом. Вы можете освободить все ресурсы, связанные с объектом, а затем вызвать **MakeInvalid,** чтобы признать недействительными все методы в унаследованных интерфейсах. Вызовы к любому из этих методов возвращаются MAPI_E_INVALID_OBJECT. Использование **MakeInvalid** — это вариант, который многие поставщики услуг предпочитают игнорировать. 
  
## <a name="see-also"></a>См. также



[Отключение поставщика услуг](shutting-down-a-service-provider.md)

