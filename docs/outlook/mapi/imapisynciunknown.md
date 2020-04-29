---
title: Имаписинк IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405594"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет механизм для синхронизации электронной почты вместо использования API транспорта. Этот интерфейс предоставляется в объекте Store. С помощью этого интерфейса и [имаписинкпрогресскаллбакк: IUnknown](imapisyncprogresscallbackiunknown.md)поставщик транспорта может предоставлять более удобные и появляющиеся сообщения об ошибках, чем те, которые отображаются в диалоговом окне отправки и получения в Microsoft Outlook.
  
Папка "Исходящие" все еще находится в хранилище по умолчанию. Outlook продолжит использовать транспортный API для отправки почты, так как исходящее сообщение не может находиться во внешнем хранилище.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Поставщики услуг хранения и транспорта  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг хранения и транспорта  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[синчронизеинбаккграунд](imapisyncsynchronizeinbackground.md) <br/> |Реализуется поставщиками хранилищ сообщений. Этот метод вызывается Outlook 2010 и Outlook 2013 для запуска синхронизации.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Интерфейсы MAPI](mapi-interfaces.md)

