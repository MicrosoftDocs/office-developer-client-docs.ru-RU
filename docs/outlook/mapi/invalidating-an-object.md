---
title: Объявление объекта недействительным
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9c0ba8f1f0bf31bb892f380df310cd9fa7a8a24f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809470"
---
# <a name="invalidating-an-object"></a>Объявление объекта недействительным

  
  
**Относится к**: Outlook 
  
В процессе завершения работы ваш поставщик необходимо объявить недействительным объекта. Аннулирование объект включает в себя заменив его vtable vtable, содержащий реализации для трех методов **IUnknown** : **AddRef**, **версии**и **QueryInterface**. Объект недействительными, вызвав [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), метод, который включен в объекте поддержку каждого из трех распространенных типов поставщиков. Поставщики обычно позвонить в реализации метода **выхода** их объекта входа в систему. 
  
Аннулирование объекта дает MAPI ultimate ответственность за освобождение памяти, связанного с объектом. Можно освободить все ресурсы, подключенных с помощью объекта и затем вызвать **MakeInvalid** на все методы в его наследуемых интерфейсов недействительными. Вызовы любого из этих методов возвращает MAPI_E_INVALID_OBJECT. С помощью **MakeInvalid** — это параметр, который многие поставщики услуг выберите игнорирование. 
  
## <a name="see-also"></a>См. также



[Завершение работы поставщика службы](shutting-down-a-service-provider.md)

