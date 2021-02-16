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
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439291"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Устарело. Возвращает типы адресов, которые могут обрабатываться всеми поставщиками транспорта в сеансе. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая указывает формат возвращаемого типа адресов. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Типы адресов имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, типы адресов имеют формат ANSI.
    
 _lpcAdrTypes_
  
> [out] Указатель на количество типов адресов, на которые указывает параметр _lpppszAdrTypes._ 
    
 _lpppszAdrTypes_
  
> [out] Указатель на массив указателей на типы адресов.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Типы адресов были успешно извлечены.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::EnumAdrTypes** возвращает список типов адресов, которые могут обрабатываться всеми активными поставщиками транспорта в сеансе. Типы адресов для поставщиков транспорта, которые в настоящее время не загружены, не включаются в список. Поставщики транспорта регистрируются для обработки одного или более типов адресов, когда MAPI вызывает метод [IXPLogon::AddressTypes.](ixplogon-addresstypes.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить массив строк, на который указывает параметр _lpppszAdrTypes._ 
  
## <a name="see-also"></a>См. также



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

