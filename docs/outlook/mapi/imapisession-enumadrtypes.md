---
title: Имаписессионенумадртипес
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338439"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устаревшие. Возвращает типы адресов, которые могут обрабатываться всеми поставщиками транспорта в сеансе. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, указывающая формат для возвращаемых типов адресов. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Типы адреса представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, типы адреса представлены в формате ANSI.
    
 _Лпкадртипес_
  
> вышли Указатель на количество типов адресов, на которые указывает параметр _лпппсзадртипес_ . 
    
 _Лпппсзадртипес_
  
> вышли Указатель на массив указателей на типы адресов.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Типы адресов успешно получены.
    
## <a name="remarks"></a>Комментарии

Метод **IMAPISession:: енумадртипес** возвращает список типов адресов, которые могут обрабатываться всеми активными поставщиками транспорта в сеансе. Типы адресов для поставщиков транспорта, которые не загружены в данный момент, не включены в список. Поставщики транспорта регистрируются для обработки одного или нескольких типов адресов, когда MAPI вызывает метод [иксплогон:: аддресстипес](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

ВыЗовите метод [мапифрибуффер](mapifreebuffer.md) , чтобы освободить массив строк, на который указывает параметр _лпппсзадртипес_ . 
  
## <a name="see-also"></a>См. также



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

