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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет функцию, которая предпроцессирует содержимое сообщения или формат сообщения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Определенные функции, реализованные в:  <br/> |Поставщики транспорта  <br/> |
|Определенная функция, вызванная:  <br/> |Шпалер MAPI  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _lpvSession_
  
> [in] Указатель на сеанс, который будет использоваться. 
    
 _lpMessage_
  
> [in] Указатель на предварительное обращение к сообщению. 
    
 _lpAdrBook_
  
> [in] Указатель на адресную книгу, из которой пользователь должен выбрать получателей для сообщения. 
    
 _lpFolder_
  
> [in, out] Указатель на папку. На входе  _параметр lpFolder_ указывает на папку, содержаную сообщения, которые необходимо предварительно процесовать. На выходе  _lpFolder_ указывает на папку, в которой размещены предварительно размещенные сообщения. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться для выделения дополнительной памяти при необходимости. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться для бесплатной памяти. 
    
 _lpcOutbound_
  
> [вышел] Указатель на количество сообщений в массиве, на которое указывает _параметр lpppMessage._ 
    
 _lpppMessage_
  
> [вышел] Указатель на указатель массива указателей для предварительной подготовки или иным образом созданных сообщений. 
    
 _lppRecipList_
  
> [вышел] Указатель на необязательный возвращенный [ADRLIST](adrlist.md) структуру, перечисление предварительно обнаруженных получателей, для которых сообщение недоставка. Дополнительные сведения о содержимом этого списка см. в методе [IMAPISupport::StatusRecips.](imapisupport-statusrecips.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Содержимое сообщений успешно было предварительно процесировали.
    
## <a name="remarks"></a>Примечания

Препроцессор сообщения транспортного поставщика может представить индикатор прогресса во время предварительной подготовки сообщения. Однако он никогда не должен представлять диалоговое окно, требующее взаимодействия с пользователем во время предварительной подготовки сообщения. 
  
Если препроцессор добавляет большие объемы данных в исходящие сообщения, необходимо следовать определенным процедурам. Этот тип сообщения может храниться в серверном хранилище сообщений, в результате чего предпроцессор может получить доступ к удаленному магазину, что занимает много времени. Чтобы этого не сделать, у препроцессора должен быть параметр, который позволяет ему хранить данные, которые занимает большое количество места в локальном хранилище сообщений, и предоставлять ссылку на этот локальный магазин в сообщении. 
  
Препроцессор не должен выпускать какие-либо объекты, первоначально переданные функции **preprocessMessage.** 
  
Прежде чем шпалер MAPI может вызвать функцию **PreprocessMessage,** поставщик транспорта должен зарегистрировать эту функцию в вызове метода [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md) После вызова **функции PreprocessMessage** шпалер не может продолжить отправку сообщения до тех пор, пока функция не вернется. 
  
Spooler MAPI владеет задачей отправки сообщений. Это означает, что исходное сообщение никогда не помещается в массив указателей сообщений и что вызов к методам **SubmitMessage** никогда не требуется. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

