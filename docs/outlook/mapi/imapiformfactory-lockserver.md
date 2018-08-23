---
title: IMAPIFormFactoryLockServer
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
ms.openlocfilehash: c4d7273b7393d421092bb06377aece0842b5fb67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590822"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сохраняет это сервер открытой формы в памяти.
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _fLockServer_
  
> [in] **значение true** для увеличения значения счетчика блокировок; в противном случае — **false**.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Средства просмотра форм вызовите метод **IMAPIFormFactory::LockServer** для хранения приложения сервера открытой формы в памяти. Поддержание сервера форм в памяти повышает эффективность своей работы, когда часто создаются и выпущен форм. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Метод **IMAPIFormFactory::LockServer** очень похож на метод [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) . В сущности метод **IMAPIFormFactory::LockServer** поддерживает вызова число сколько раз; Поскольку это число больше 0, метод предотвращает выгрузки из памяти сервера форм. Чтобы реализовать ее можно использовать функцию [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) . 
  
## <a name="see-also"></a>См. также



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

