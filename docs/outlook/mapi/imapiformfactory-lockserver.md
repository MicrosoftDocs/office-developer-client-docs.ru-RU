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
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389059"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Средства просмотра форм вызовите метод **IMAPIFormFactory::LockServer** для хранения приложения сервера открытой формы в памяти. Поддержание сервера форм в памяти повышает эффективность своей работы, когда часто создаются и выпущен форм. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Метод **IMAPIFormFactory::LockServer** очень похож на метод [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) . В сущности метод **IMAPIFormFactory::LockServer** поддерживает вызова число сколько раз; Поскольку это число больше 0, метод предотвращает выгрузки из памяти сервера форм. Чтобы реализовать ее можно использовать функцию [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) . 
  
## <a name="see-also"></a>См. также



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

