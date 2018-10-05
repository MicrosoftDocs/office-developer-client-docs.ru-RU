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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382549"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет поставщику хранилища файлов (PST) личных папок для переопределения политики PSTDisableGrow.
  
|||
|:-----|:-----|
|Наследует от:  <br/> |Интерфейс IUnknown  <br/> |
|Реализовано в:  <br/> |Поставщик хранения PST-файлов  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Получение списка регистраций для файл личных папок (PST).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Регистрирует файлы личных папок для автоматического разблокирование Предотвращение дальнейшие вызовы HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Разблокирует файл личных папок для роста.  <br/> |
   
## <a name="remarks"></a>Замечания

Идентификаторы интерфейса обработчик переопределить PST-файлов не могут быть определены в файле загружаемых заголовка, которое имеется в настоящее время, в этом случае будет получить в разделе [Константы MAPI](mapi-constants.md) и можно скопировать и добавьте их в коде. Используйте макрос DEFINE_GUID определенные в guiddef.h файл заголовка Microsoft Windows Software Development Kit (SDK) для сопоставления имен символьной глобальный уникальный идентификатор (GUID) с их значениями. 
  
Дополнительные сведения см в [реализации обработчика переопределение PST-файлов для обхода политики PSTDisableGrow в Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

