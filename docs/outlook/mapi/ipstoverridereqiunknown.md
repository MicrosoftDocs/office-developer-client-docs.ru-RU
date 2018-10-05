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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389108"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поставщик хранилища доступ к ресурсам файл личных папок (PST).
  
|||
|:-----|:-----|
|Наследует от:  <br/> |Интерфейс IUnknown  <br/> |
|Реализовано в:  <br/> |Поставщик хранения PST-файлов  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Инициирует разблокировка процедура файл личных папок (PST).  <br/> |
   
## <a name="remarks"></a>Замечания

Идентификаторы интерфейса обработчик переопределить PST-файлов не могут быть определены в файле загружаемых заголовка, которое имеется в настоящее время, в этом случае будет получить в разделе [Константы MAPI](mapi-constants.md) и можно скопировать и добавьте их в коде. Используйте макрос DEFINE_GUID определенные в guiddef.h файл заголовка Microsoft Windows Software Development Kit (SDK) для сопоставления имен символьной глобальный уникальный идентификатор (GUID) с их значениями. 
  
Дополнительные сведения см в [реализации обработчика переопределение PST-файлов для обхода политики PSTDisableGrow в Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

