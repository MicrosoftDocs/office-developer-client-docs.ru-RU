---
title: ИПСТОВЕРРИДЕРЕК IUnknown
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
  
Получает доступ к ресурсам поставщика хранилища файлов личных папок (PST).
  
|||
|:-----|:-----|
|Наследование от:  <br/> |Интерфейс  <br/> |
|Реализовано в:  <br/> |Поставщик хранилища PST  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Инициирует процедуру разблокировки для файла личных папок (PST).  <br/> |
   
## <a name="remarks"></a>Примечания

Идентификаторы интерфейса обработчика переопределения PST-файлов могут быть не определены в текущем загружаемом файле заголовков, в этом случае вы найдете их в разделе [константы MAPI](mapi-constants.md) и можете скопировать их в свой код. Используйте макрос ДЕФИНЕ_ГУИД, определенный в файле заголовков пакета средств разработки программного обеспечения (SDK) для Microsoft Windows (SDK) guiddef. h, для сопоставления псевдонимов глобального уникального идентификатора (GUID) с их значениями. 
  
Для получения дополнительных сведений Узнайте, [как реализовать обработчик переопределения PST-файлов, чтобы обойти политику пстдисаблегров в Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

