---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6bd13eb7180302a5ab770586cf36856ca5a22676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809056"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Относится к**: Outlook 
  
Рекомендуется использовать. Возвращает типы адресов, которые могут быть обработаны всеми поставщиками транспорта в сеансе. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, которое указывает формат для типов возвращаемых адресов. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Типы адресов, в формате Юникод. Если флаг MAPI_UNICODE не установлен, типы адресов, в формате ANSI.
    
 _lpcAdrTypes_
  
> [out] Указатель на число типов адрес, на который указывает параметр _lpppszAdrTypes_ . 
    
 _lpppszAdrTypes_
  
> [out] Указатель на массив указатели на типов адресов.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Типы адресов были успешно извлечен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::EnumAdrTypes** возвращает список типов адресов, которые могут быть обработаны всеми поставщиками транспорта активный в сеансе. Типы адресов для поставщиков транспорта, которые не загружаются в настоящее время не включаются в списке. Поставщики транспорта зарегистрировать для обработки один или несколько типов адресов при MAPI вызывает метод их [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов [MAPIFreeBuffer](mapifreebuffer.md) для освобождения массив строк, на который указывает параметр _lpppszAdrTypes_ . 
  
## <a name="see-also"></a>См. также



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

