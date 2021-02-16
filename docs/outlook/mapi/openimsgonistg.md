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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает новый объект [IMessage](imessageimapiprop.md) поверх существующего объекта OLE **IStorage,** который будет использоваться в сеансе сообщения. 
  
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

## <a name="parameters"></a>Параметры

_lpMsgSess_
  
> [in] Указатель на объект сеанса сообщения, в котором должен быть создан новый объект **IMessage** **-on-IStorage.** 
    
_lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти. 
    
_lpAllocateMore_
  
> [in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти. 
    
_lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память. 
    
_lpMalloc_
  
> [in] Указатель на объект-память для размещения интерфейса OLE **IMalloc.** Интерфейс **IMessage** должен использовать этот метод выделения при работе с такими интерфейсами, как **IStorage** и **IStream.** 
    
_lpMapiSup_
  
> [in] Необязательный указатель на объект поддержки MAPI, который поставщик службы может использовать для вызова методов [интерфейса IMAPISupport : IUnknown.](imapisupportiunknown.md) 
    
_lpStg_
  
> [in, out] Указатель на открытый объект OLE **IStorage** с разрешением только для чтения или чтения и записи. Так **как IMessage** не поддерживает доступ только для записи, **OpenIMsgOnIStg** не принимает объект хранилища, открытый в режиме только для записи. 
    
_lpfMsgCallRelease_
  
> [in] Необязательный указатель на функцию вызова на основе прототипа [MSGCALLRELEASE,](msgcallrelease.md) который MAPI должен вызывать после последнего выпуска объекта **IMessage**-on-IStorage.  
    
_ulCallerData_
  
> [in] Данные вызываемого объекта, сохраненные с помощью MAPI с объектом **IMessage** **-on-IStorage** и переданные функции вызова на основе **MSGCALLRELEASE.** Данные предоставляют контекст об **освобожденных объектах IMessage** и **объекте IStorage,** поверх которого он был создан. 
    
_ulFlags_
  
> [in] Битовая почта флагов, используемая для управления вызовом метода OLE **IStorage::Commit,** когда клиентские приложения или поставщик службы вызывает метод **IMessage::SaveChanges.** Можно установить следующие флаги: 
    
IMSG_NO_ISTG_COMMIT 
  
> Метод OLE **IStorage::Commit** не вызывается, когда клиент или поставщик вызывает [SaveChanges.](imapiprop-savechanges.md) 
    
MAPI_UNICODE
  
> Позволяет создавать MSG-файлы Юникода. В [итоговом файле IMessage](imessageimapiprop.md) STORE_UNICODE_OK в [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) поддерживаются свойства Юникод. 
    
  > [!NOTE]
  > Флаг MAPI_UNICODE поддерживается только в этой функции в Outlook 2003 или более высоких уровнях. 
  
_lppMsg_
  
> [out] Указатель на указатель на открытый **объект IMessage.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Доступ к атрибутам свойств можно получить только для объектов свойств, то есть объектов, реализующих [интерфейс IMAPIProp : IUnknown.](imapipropiunknown.md) Чтобы сделать свойства MAPI доступными для объекта OLE структурированного хранилища, **OpenIMsgOnIStg** создает [объект IMessage : IMAPIProp](imessageimapiprop.md) поверх объекта OLE **IStorage.** Атрибуты свойств для таких объектов можно установить или изменить с помощью [SetAttribIMsgOnIStg](setattribimsgonistg.md) и получить с помощью [GetAttribIMsgOnIStg.](getattribimsgonistg.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Перед тем как будет вызван **OpenIMsgOnIStg,** необходимо открыть сеанс сообщения с помощью [OpenIMsgSession.](openimsgsession.md) Если предоставить допустимый  _параметр lpMsgSess,_ новое сообщение будет создано в течение сеанса сообщения, чтобы оно было закрыто при закрытии сеанса. Если  _lpMsgSess_ имеет NULL, сообщение создается независимо от сеанса сообщения. Если клиентского приложения или поставщика услуг, создав сообщение не освобождает его, а также все его вложения и открытые таблицы, утечка памяти и может привести к завершению приложения. 
  
MAPI использует функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения и распределения памяти, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Указатели _lpAllocateBuffer,_ _lpAllocateMore_ и _lpFreeBuffer_ являются необязательными, если функция **OpenIMsgOnIStg** вызвана с допустимым параметром _lpMapiSup._ 
  
Так как он имеет дело с объектом OLE, MAPI также должен использовать выделение памяти OLE. Дополнительные сведения о структурированных объектах хранения OLE и выделении памяти OLE см. в справочнике _по OLE Programmer._ 
  
Если для _lpMapiSup_ задается действительное значение, **IMessage** поддерживает флаги MAPI_DIALOG и ATTACH_DIALOG путем вызова метода [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) для обеспечения пользовательского интерфейса хода выполнения для методов [IMAPIProp::CopyTo](imapiprop-copyto.md) и [IMessage::D eleteAttach.](imessage-deleteattach.md) Кроме того, метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) пытается преобразовать краткосрочные идентификаторы записей в долгосрочные идентификаторы записей, вызывая метод [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) и вызывая итоговый объект адресной книги. Если для  _lpMapiSup_ передается NULL, **IMessage** игнорирует MAPI_DIALOG и ATTACH_DIALOG и сохраняет краткосрочные идентификаторы записей без преобразования. 
  
Объект **IStorage,** на который указывает параметр  _lpStg,_ должен быть открыт в режиме STGM_READ или STGM_READWRITE режиме. Если используется STGM_READWRITE, необходимо также STGM_TRANSACTED режиме. 
  
Функция callback, на которая указывает параметр _lpfMsgCallRelease,_ является необязательной; Если он предоставлен, он должен быть основан на прототипе функции [MSGCALLRELEASE.](msgcallrelease.md) Интерфейс **IMessage** вызывает его, когда для отсчета объекта **IMessage**-on-IStorage задается нулевое значение при последнем вызове метода **Release.**  Функция callback обычно используется для освободить интерфейс **IStorage.** **IMessage** не будет пытаться получить доступ к объекту **IStorage,** на который указывает параметр  _lpStg_ после вызова. 
  
Некоторые клиенты или поставщики могут записывать дополнительные данные в объект **IStorage** помимо записи **IMessage** при его методе [SaveChanges.](imapiprop-savechanges.md) Клиент или поставщик может использовать флаг IMSG_NO_ISTG_COMMIT, чтобы запретить **IMessage** вызывать метод OLE **IStorage::Commit** при обработке вызова **SaveChanges;** в этом случае клиент или поставщик должен сам зафиксировать **объект IStorage** при написании дополнительных данных. Для этого реализация **IMessage** гарантирует, что все подкатеголи, которые она создает в объекте **IStorage,** начинаются со строки "__", то есть с двумя подчеркиваниями. Клиент или поставщик могут избежать конфликтующих имен, не выходя из этого пространства имен. 
  
MAPI не определяет поведение нескольких операций открытия, выполняемой в подобекте сообщения, например вложения, потока или внедренного сообщения. MapI в настоящее время позволяет открыть подобект, который уже открыт, еще раз, но MAPI выполняет операцию открытия, повысив количество ссылок для существующего открытого объекта и вернув его клиенту или поставщику, который вызвал [метод IMessage::OpenAttach](imessage-openattach.md) или [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Это означает, что для первой операции открытия в подобъекте запрашивается доступ, предоставляемый для всех последующих операций открытия, независимо от доступа, запрашиваемого операциями. 
  
Правильная процедура размещения сообщения во вложении заключается в вызове метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором интерфейса IID_IMessage. **В настоящее время OpenProperty** также поддерживает создание вложений сообщений, доступных непосредственно в интерфейсе OLE **IStorage,** то есть с помощью идентификатора IID_IStorage интерфейса. **Доступ IStorage** поддерживается, чтобы обеспечить простой способ поместить документ Microsoft Word во вложение без его преобразования в интерфейс OLE **IStream** или из него. Однако **IMessage** может вести себя предсказуемо, если **OpenIMsgOnIStg** передает указатель **IStorage** на данные вложения, а затем объекты отпущены в неправильном порядке. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI использует метод **OpenIMsgOnIStg** для открытия интерфейса IMessage поверх . MSG-файл для обработки файла с помощью MAPI.  <br/> |
   
## <a name="see-also"></a>См. также

- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

