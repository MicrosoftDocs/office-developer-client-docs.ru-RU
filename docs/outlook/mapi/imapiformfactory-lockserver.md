---
title: Имапиформфакторилокксервер
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342142"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сохраняет открытый сервер форм в памяти.
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Флокксервер_
  
> возврата **значение true** , чтобы увеличить число блокировок; в противном случае — **false**.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Комментарии

Средства просмотра форм вызывают метод **имапиформфактори:: локксервер** , чтобы сохранить открытое приложение в памяти для сервера. Хранение сервера форм в памяти повышает производительность, когда формы часто создаются и освобождаются. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Метод **имапиформфактори:: локксервер** очень похож на метод [IClassFactory:: локксервер](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) . По сути, метод **имапиформфактори:: локксервер** поддерживает количество вызовов, которые он вызывал; пока значение счетчика больше 0, метод предотвращает выгрузку сервера форм из памяти. Для реализации этого параметра можно использовать функцию [колоккобжектекстернал](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) . 
  
## <a name="see-also"></a>См. также



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

