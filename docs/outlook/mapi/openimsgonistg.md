---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406523"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает новый [объект IMessage](imessageimapiprop.md) поверх существующего объекта **IStorage** OLE, который будет использоваться в сеансе сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a>Parameters

_lpMsgSess_
  
> [in] Указатель на объект сеанса сообщений, в котором должен быть создан новый объект **IMessage-on-IStorage.**  
    
_lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти. 
    
_lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться для выделения дополнительной памяти. 
    
_lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться для бесплатной памяти. 
    
_lpMalloc_
  
> [in] Указатель на объект-аллигатор памяти, подвергая обнажает интерфейс OLE **IMalloc.** Интерфейс **IMessage** должен использовать этот метод выделения при работе с такими интерфейсами, как **IStorage** и **IStream.** 
    
_lpMapiSup_
  
> [in] Необязательный указатель на объект поддержки MAPI, который поставщик служб может использовать для вызова методов [интерфейса IMAPISupport: IUnknown.](imapisupportiunknown.md) 
    
_lpStg_
  
> [in, out] Указатель на открытый объект **IStorage** OLE, который имеет разрешение только для чтения или чтения или записи. Так **как IMessage** не поддерживает доступ только для записи, **OpenIMsgOnIStg** не принимает объект хранения, открытый в режиме только для записи. 
    
_lpfMsgCallRelease_
  
> [in] Необязательный указатель на функцию вызова на основе прототипа [MSGCALLRELEASE,](msgcallrelease.md) который MAPI должен вызывать после последнего выпуска на **объекте IMessage-on-IStorage.**  
    
_ulCallerData_
  
> [in] Данные вызываемого звонка, сохраненные MAPI с **объектом IMessage-on-IStorage** и переданы функции вызова на основе **MSGCALLRELEASE.**  Данные предоставляют контекст **выпускаемого объекта IMessage** и **объекта IStorage,** поверх которого он был построен. 
    
_ulFlags_
  
> [in] Bitmask флагов, используемых для контроля, вызывается ли метод OLE **IStorage::Commit,** когда клиентская заявка или поставщик услуг вызывает **метод IMessage::SaveChanges.** Можно установить следующие флаги: 
    
IMSG_NO_ISTG_COMMIT 
  
> Метод OLE **IStorage::Commit** не вызывается, когда клиент или поставщик вызывает [SaveChanges.](imapiprop-savechanges.md) 
    
MAPI_UNICODE
  
> Включает создание файлов Unicode .msg. В результате [файл IMessage](imessageimapiprop.md) STORE_UNICODE_OK в [](pidtagstoresupportmask-canonical-property.md) PR_STORE_SUPPORT_MASK поддерживает свойства Unicode. 
    
  > [!NOTE]
  > Флаг MAPI_UNICODE поддерживается только в этой функции Outlook 2003 или выше. 
  
_lppMsg_
  
> [вышел] Указатель на указатель на открытый **объект IMessage.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Атрибуты свойств можно получить только для объектов свойств, то есть объектов, реализующих [интерфейс IMAPIProp : IUnknown.](imapipropiunknown.md) Чтобы сделать свойства MAPI доступными для структурированного объекта хранения OLE, **OpenIMsgOnIStg** создает [объект IMessage : IMAPIProp](imessageimapiprop.md) поверх объекта **IStorage** OLE. Атрибуты свойств таких объектов можно установить или изменить с [помощью SetAttribIMsgOnIStg](setattribimsgonistg.md) и получить с [помощью GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Сеанс сообщения следует открыть с [помощью OpenIMsgSession](openimsgsession.md) перед тем, как будет вызван **OpenIMsgOnIStg.** При поставке допустимой  _lpMsgSess_ параметр убедитесь, что новое сообщение создается в сеансе сообщений, чтобы оно было закрыто при закрытии сеанса. Если  _lpMsgSess_ является NULL, сообщение создается независимо от сеанса сообщений. Если клиент-приложение или поставщик услуг, создав сообщение, не выпускает его, а также все его вложения и открытые таблицы, происходит утечка памяти и может привести к прекращению работы приложения. 
  
MAPI использует функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для большинства распределений памяти и распределения, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Указатели _lpAllocateBuffer,_ _lpAllocateMore_ и _lpFreeBuffer_ необязательны, если функция **OpenIMsgOnIStg** вызвана с допустимым _параметром lpMapiSup._ 
  
Так как он имеет дело с объектом OLE, MAPI также необходимо использовать распределение памяти OLE. Дополнительные сведения о структурированных объектах хранения OLE и распределении памяти OLE см. в справке программиста _OLE._ 
  
Если для _lpMapiSup_ предоставляется допустимые значения, **IMessage** поддерживает флаги MAPI_DIALOG и ATTACH_DIALOG, вызывая метод [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) для обеспечения пользовательского интерфейса прогресса для методов [IMAPIProp::CopyTo](imapiprop-copyto.md) и [IMessage::D eleteAttach.](imessage-deleteattach.md) Кроме того, метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) пытается преобразовать краткосрочные идентификаторы записи в долгосрочные идентификаторы записи, позвонив по методу [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) и сделав вызовы на вызываемом объекте адресной книги. Если NULL передается для  _lpMapiSup,_ **IMessage** игнорирует MAPI_DIALOG и ATTACH_DIALOG и сохраняет краткосрочные идентификаторы записи без преобразования. 
  
Объект **IStorage,** на который указывает параметр  _lpStg,_ должен быть открыт в режиме STGM_READ или STGM_READWRITE. Если используется STGM_READWRITE режим, STGM_TRANSACTED должен быть установлен режим STGM_TRANSACTED. 
  
Функция вызова, на что указывает параметр _lpfMsgCallRelease,_ необязательна; при условии, он должен основываться на прототипе [функции MSGCALLRELEASE.](msgcallrelease.md) Интерфейс **IMessage** вызывает его, когда отсчет ссылок объекта **IMessage-on-IStorage** установлен до нуля последним вызовом метода **выпуска.**  Функция вызова обычно используется для бесплатного интерфейса **IStorage.** **После вызова IMessage** не будет пытаться получить доступ к объекту **IStorage,** на который указывает параметр _lpStg._ 
  
Некоторые клиенты или поставщики могут записывать дополнительные данные на **объект IStorage,** помимо того, что сам **IMessage** записывает, когда называется метод [SaveChanges.](imapiprop-savechanges.md) Клиент или поставщик могут использовать флаг IMSG_NO_ISTG_COMMIT, чтобы запретить **IMessage** вызывать метод OLE **IStorage::Commit** при обработке вызова **SaveChanges;** в этом случае клиент или поставщик должен сам совершить **объект IStorage** при написании дополнительных данных. Чтобы помочь в этом, **реализация IMessage** гарантирует имя всех подразрядов, которые он создает в **объекте IStorage,** начиная со строки "__", то есть с двумя подчеркиваниями. Клиент или поставщик могут избежать столкновений с именами, не выходя из этого пространства имен. 
  
MAPI не определяет поведение нескольких открытых операций, выполняемых на подобекте сообщения, таких как вложение, поток или встроенное сообщение. В настоящее время MAPI позволяет открыть уже открытый субобект, но MAPI выполняет открытую операцию путем прибавления отсчета ссылок для существующего открытого объекта и его возврата клиенту или поставщику, который вызвал [метод IMessage::OpenAttach](imessage-openattach.md) или [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Это означает, что доступ, запрашиваемый для первой открытой операции на подобъекте, — это доступ, предоставляемый для всех последующих открытых операций, независимо от доступа, запрашиваемого операциями. 
  
Правильная процедура размещения сообщения в вложения заключается в вызове [метода IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором интерфейса IID_IMessage. **В настоящее время OpenProperty** также поддерживает создание вложений сообщений, доступных непосредственно в интерфейсе **IStorage** OLE, то есть с помощью идентификатора IID_IStorage интерфейса. **Доступ к IStorage** поддерживается, чтобы разрешить простой способ поместить документ Microsoft Word в вложение без преобразования его в интерфейс OLE **IStream** или из него. Тем не **менее, IMessage** может вести себя не предсказуемо, если **OpenIMsgOnIStg** передает указатель **IStorage** на данные вложения, а затем объекты будут выпущены в неправильном порядке. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI использует **метод OpenIMsgOnIStg** для открытия интерфейса IMessage поверх . MsG-файл, чтобы управлять файлом с помощью MAPI.  <br/> |
   
## <a name="see-also"></a>См. также

- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

