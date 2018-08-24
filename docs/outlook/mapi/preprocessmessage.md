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
ms.openlocfilehash: 878c3aaf22a6cf8a08c8234df41b671088c435c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584991"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет функцию, которая выполняет предварительную обработку содержимое сообщения или формат сообщения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Функция реализован:  <br/> |Поставщиками транспорта  <br/> |
|Вызывается функция:  <br/> |Диспетчер очереди MAPI  <br/> |
   
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
  
> [in] Указатель для использования в сеансе. 
    
 _lpMessage_
  
> [in] Указатель на сообщение, чтобы быть предварительной обработки. 
    
 _lpAdrBook_
  
> [in] Указатель в адресную книгу, из которого пользователь должен выбрать получателей сообщения. 
    
 _lpFolder_
  
> [in, out] Указатель на папку. На входе параметр _lpFolder_ указывает на папку, содержащую сообщения, чтобы быть предварительной обработки. На выходе _lpFolder_ указывает на папку, где размещен предварительной обработки сообщений. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти там, где необходимо. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти. 
    
 _lpcOutbound_
  
> [out] Указатель на количество сообщений в массиве указывает параметр _lpppMessage_ . 
    
 _lpppMessage_
  
> [out] Указатель на указатель на массив указатели на предварительно или в противном случае создается сообщения. 
    
 _lppRecipList_
  
> [out] Указатель на необязательный возвращенные [ADRLIST](adrlist.md) структуру, список обнаруженных препроцессор получателей, для которых не удается доставить сообщение. Дополнительные сведения о содержимом этого списка [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) см. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Содержимое сообщения были успешно обработаны.
    
## <a name="remarks"></a>Замечания

Препроцессор поставщика транспорта сообщений можно представить индикатор хода выполнения во время предварительной обработки сообщения. Тем не менее он никогда не должно представлять диалоговое окно, требующее вмешательства пользователя во время предварительной обработки сообщения. 
  
Когда препроцессор добавляет больших объемов данных в исходящее сообщение, рекомендуется придерживаться определенных процедур. Этот тип сообщения могут храниться в хранилище сообщений на стороне сервера, вследствие чего препроцессор для доступа к удаленного хранилища продолжительное время. Чтобы избежать этого, препроцессор должен иметь возможность, позволяющая его для хранения данных, который занимает большой объем пространства в хранилище локального сообщения и предоставить ссылку на этот локального хранилища в сообщении. 
  
Не освобождать препроцессор какие-либо объекты, изначально переданных функции **PreprocessMessage** на основе. 
  
Прежде чем диспетчер очереди MAPI можно вызвать функцию **PreprocessMessage** , поставщика транспорта необходимо зарегистрировать в вызове метода [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) функцию. После вызова функции **PreprocessMessage** , диспетчер очереди не может продолжать работу отправки сообщения, пока не функция возвращает. 
  
Диспетчер очереди MAPI несет ответственность за задачу отправка сообщений. Это означает исходного сообщения никогда не переводится в массив указателей сообщение и вызвать методы **SubmitMessage** не требуется. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

