---
title: Имапиформадвисе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329486"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует средство просмотра форм для уведомлений о событиях, влияющих на форму.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Параметры

 _Падвисе_
  
> возврата Указатель на объект приемника уведомлений о просмотре для получения последующих уведомлений. 
    
 _Пулконнектион_
  
> вышли Указатель на ненулевое значение, представляющее успешную регистрацию уведомлений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация выполнена успешно.
    
E_OUTOFMEMORY 
  
> Не удалось выполнить регистрацию из-за недостатка памяти.
    
## <a name="remarks"></a>Комментарии

Средства просмотра форм вызывают метод формы **имапиформ:: Advise** для регистрации уведомлений об изменениях формы. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Сохраните копию указателя приемника уведомлений о просмотре, переданной в параметре _падвисе_ , чтобы можно было использовать его для вызова соответствующего метода [имапивиевадвисесинк](imapiviewadvisesinkiunknown.md) при возникновении события. ВыЗовите метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) приемника уведомлений о просмотре, чтобы сохранить указатель до отмены регистрации уведомления. Задайте для параметра _пулконнектион_ значение ненулевое значение. 
  
Многие формы реализуют вспомогательный объект для обработки регистрации и последующего уведомления о событиях. 
  
Дополнительные сведения о процессе уведомления в разделе Общие сведения об уведомлении о [событиях в MAPI](event-notification-in-mapi.md). 
  
Дополнительные сведения об уведомлении и формах можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>См. также



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Уведомление о соБытии в MAPI](event-notification-in-mapi.md)
  
[Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md)

