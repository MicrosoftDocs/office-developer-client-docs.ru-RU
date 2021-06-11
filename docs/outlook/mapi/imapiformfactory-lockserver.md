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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342142"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сохраняет открытый сервер формы в памяти.
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _fLockServer_
  
> [in] **верно** для приумно-ления счета блокировки; в противном **случае, false**.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Зрители форм называют **метод IMAPIFormFactory::LockServer** для сохраняемого приложения сервера формы в памяти. Сохранение сервера форм в памяти повышает его производительность, когда формы часто создаются и выпускаются. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Метод **IMAPIFormFactory::LockServer** очень похож на [метод IClassFactory::LockServer.](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) По сути, метод **IMAPIFormFactory::LockServer** поддерживает подсчет, сколько раз он был вызван; до тех пор, пока это количество превышает 0, метод предотвращает выгрузку сервера форм из памяти. Для реализации этой функции можно использовать функцию [CoLockObjectExternal.](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) 
  
## <a name="see-also"></a>См. также



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

