---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: e66d48b6caefe0fee67f41ea829db3201751cf27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808668"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**Применимо к**: Outlook 
  
Разделяет составные запись идентификатор объекта, обычно сообщения в банке сообщений в идентификатор записи этого объекта в хранилище и идентификатор записи хранилища.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Parameters

 _psession_
  
> [in] Указатель на сеанс используется клиентским приложением. 
    
 _cbEID_
  
> [in] Размер, в байтах, составные запись идентификатора отделить. 
    
 _pEID_
  
> [in] Указатель на идентификатор составные записи отделить. 
    
 _pcbStoreEID_
  
> [out] Указатель на возвращаемый размер, в байтах, идентификатор записи хранилища сообщение, содержащее объект. Если параметр _pEID_ указывает идентификатор noncompound записи, параметр _pcbStoreEID_ указывает нулевое значение. 
    
 _ppStoreEID_
  
> [out] Указатель на указатель на идентификатор возвращенного элемента хранилища сообщение, содержащее объект. Если параметр _pEID_ указывает идентификатор noncompound записи, с помощью параметра _ppStoreEID_ возвращается значение NULL. 
    
 _pcbMsgEID_
  
> [out] Указатель на возвращаемый размер, в байтах, запись идентификатор объекта. Если параметр _pEID_ указывает идентификатор noncompound записи, параметр _pcbMsgEID_ равно значению параметра _cbEID_ . 
    
 _ppMsgEID_
  
> [out] Указатель на указатель возвращенного элемента идентификатор объекта. Если параметр _pEID_ указывает идентификатор noncompound записи, _ppMsgEID_ указывает указатель на копию идентификатор noncompound записи. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Если идентификатор, указанный в параметре _pEID_ составные, она разбивается на идентификатор записи объекта в его хранилища сообщений и идентификатор записи хранилища. Строки идентификатора noncompound записи, просто копируются. Составные идентификатор отделить обычно является одним создан с помощью функции [HrComposeEID](hrcomposeeid.md) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Объем памяти, в котором размещается параметр _pEID_ высвобождается при успешном выполнении этой функции. Вызывающий реализации несет ответственность за освобождение памяти для выходных параметров. 
  

