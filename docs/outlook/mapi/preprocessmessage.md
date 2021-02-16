---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437247"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет функцию, которая предварительно обучает содержимое сообщения или его формат.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Определяемая функция, реализованная в:  <br/> |Поставщики транспорта  <br/> |
|Определяемая функция, вызванная:  <br/> |MapI spooler  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a>Параметры

 _lpvSession_
  
> [in] Указатель на используемый сеанс. 
    
 _lpMessage_
  
> [in] Указатель на сообщение для предварительной подготовки. 
    
 _lpAdrBook_
  
> [in] Указатель на адресную книгу, из которой пользователь должен выбрать получателей сообщения. 
    
 _lpFolder_
  
> [in, out] Указатель на папку. При вводе  _параметр lpFolder_ указывает на папку, содержаную сообщения для предварительной подготовки. При выходе  _lpFolder_ указывает на папку, в которой были размещены предварительно пропроцессные сообщения. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая при необходимости используется для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память. 
    
 _lpcOutbound_
  
> [out] Указатель на количество сообщений в массиве, на которое указывает параметр _lpppMessage._ 
    
 _lpppMessage_
  
> [out] Указатель на указатель на массив указателей для предварительной подготовки или других сообщений. 
    
 _lppRecipList_
  
> [out] Указатель на необязательные возвращаемые [структуры ADRLIST,](adrlist.md) перечисляя предварительно обнаруженных получателей, для которых сообщение не может быть недоставка. Дополнительные сведения о содержимом этого списка см. в методе [IMAPISupport::StatusRecips.](imapisupport-statusrecips.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Содержимое сообщений было успешно предварительно обоблюдно.
    
## <a name="remarks"></a>Примечания

Препроцессор сообщения поставщика транспорта может представить индикатор хода выполнения во время предварительной подготовки сообщения. Однако в нем никогда не должно присутствовать диалоговое окно, требующее взаимодействия с пользователем во время предварительной подготовки сообщения. 
  
Если препроцессор добавляет большие объемы данных в исходящие сообщения, следует следовать определенным процедурам. Сообщения такого типа могут храниться в серверном хранилище сообщений, что приводит к отнимаемой времени процедуре, которая занимает много времени у препроцессора. Чтобы избежать этого, предпроцессор должен иметь возможность хранить данные, которые занимает большой объем места в локальном хранилище сообщений, и предоставлять ссылку на это локальное хранилище в сообщении. 
  
Препроцессор не должен освободить какие-либо объекты, изначально переданные функции на основе **PreprocessMessage.** 
  
Прежде чем пулер MAPI может вызвать функцию **PreprocessMessage,** поставщик транспорта должен зарегистрировать эту функцию в вызове метода [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md) После вызова **функции PreprocessMessage** пул не сможет продолжить отправку сообщения, пока функция не вернется. 
  
Задача отправки сообщений принадлежит пулу MAPI. Это означает, что исходное сообщение никогда не помещается в массив указателей сообщений, а вызов методов **SubmitMessage** никогда не требуется. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

