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
ms.openlocfilehash: 56e663ced33da933b4276911b609f2fae1c5d78e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563969"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает новый объект [IMessage](imessageimapiprop.md) поверх существующего объекта OLE **IStorage** , для использования в рамках сеанса сообщения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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
  
> [in] Указатель на объект сеанса сообщения, в котором должен быть создан новый **IMessage** **IStorage** объект - on. 
    
_lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти. 
    
_lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти. 
    
_lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти. 
    
_lpMalloc_
  
> [in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** . Интерфейс **IMessage** должен использовать этот метод для распределения при работе с интерфейсами, такие как **IStorage** и **IStream**. 
    
_lpMapiSup_
  
> [in] Необязательный указатель на объект поддержки MAPI, поставщик службы можно использовать для вызова методов [IMAPISupport: IUnknown](imapisupportiunknown.md) интерфейса. 
    
_lpStg_
  
> [in, out] Указатель на объект OLE **IStorage** открытой и только для чтения или разрешение чтения и записи. Так как **IMessage** не поддерживает доступ только для записи, **OpenIMsgOnIStg** не принимает объект хранилища, открытых в режиме только для записи. 
    
_lpfMsgCallRelease_
  
> [in] Необязательный указатель на функцию обратного вызова на основании прототип [MSGCALLRELEASE](msgcallrelease.md) , MAPI для вызова после последнего выпуска **IMessage**- on - **IStorage** объекта. 
    
_ulCallerData_
  
> [in] Данные вызывающего раз сохранена с MAPI с объектом **IStorage** **IMessage**- on - и передается **MSGCALLRELEASE** на основе функции обратного вызова. Данные предоставляет контекст об объекте **IMessage** освобождения и объект **IStorage** , на котором он был создан. 
    
_ulFlags_
  
> [in] Битовая маска флаги определять, когда клиентское приложение или поставщик услуг вызывает метод **IMessage::SaveChanges** вызывается метод OLE **IStorage::Commit** . Можно задать следующие флажки: 
    
IMSG_NO_ISTG_COMMIT 
  
> Метод OLE **IStorage::Commit** — не будет вызываться, когда клиента или поставщика вызывает [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE
  
> Позволяет создавать файлы MSG-файл в кодировке Юникод. Созданный файл [IMessage](imessageimapiprop.md) показывает STORE_UNICODE_OK в его [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) и поддерживает Юникод свойства. 
    
  > [!NOTE]
  > Флаг MAPI_UNICODE поддерживается только в этой функции в Outlook 2003 или выше. 
  
_lppMsg_
  
> [out] Указатель на указатель на объект открыт **IMessage** . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Свойство атрибуты осуществляется только на свойство объекты, то есть, реализация [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейса. Чтобы сделать свойства MAPI на объект структурированного хранилища OLE, обеспечивающая **OpenIMsgOnIStg** [IMessage: IMAPIProp](imessageimapiprop.md) объекта поверх объекта OLE **IStorage** . Атрибуты свойств для таких объектов можно задать или изменены с помощью [SetAttribIMsgOnIStg](setattribimsgonistg.md) и получены с [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

До вызова **OpenIMsgOnIStg** с [OpenIMsgSession](openimsgsession.md) открывать сообщение сеанса. Допустимый _lpMsgSess_ параметра сделать sures, создано новое сообщение в рамках сеанса сообщения, чтобы он закрывается при закрытии сеанса. Если _lpMsgSess_ имеет значение NULL, независимо от любого сеанса сообщения создается сообщение. Если клиентское приложение или поставщика услуг, создавшего сообщение не освободить его, а также все вложения, откройте таблицы памяти является утечка и может привести к завершению работы приложения. 
  
Функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти, в частности для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объектной использует MAPI Например, [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). При вызове функции **OpenIMsgOnIStg** с параметром допустимый _lpMapiSup_ указатели _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ являются необязательными. 
  
Так как иметь дело с базовым объектом OLE, MAPI также необходимо использовать выделения памяти для OLE. Дополнительные сведения об объектах СТРУКТУРИРОВАННОГО хранилища и выделение памяти OLE можно _OLE Справочник программиста_. 
  
Если для _lpMapiSup_допустимое значение указано, **IMessage** поддерживает флаги MAPI_DIALOG и ATTACH_DIALOG путем вызова метода [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) , чтобы предоставить интерфейс пользователя о ходе выполнения для [IMAPIProp::CopyTo](imapiprop-copyto.md) и [IMessage::DeleteAttach](imessage-deleteattach.md) методы. Кроме того метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) пытается преобразовать краткосрочных идентификаторы записей для долгосрочного идентификаторы записей путем вызова метода [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) и выполнение вызовов на полученный объект адресной книги. Если передается _lpMapiSup_, **IMessage** игнорирует MAPI_DIALOG и ATTACH_DIALOG и сохраняет краткосрочных идентификаторы записей без преобразования. 
  
Объект **IStorage** , указанный с помощью параметра _lpStg_ необходимо открыть в режиме STGM_READ или STGM_READWRITE. Если используется режим STGM_READWRITE, необходимо также установить режим STGM_TRANSACTED. 
  
Функция обратного вызова, на который указывает параметр _lpfMsgCallRelease_ является необязательным; Если этот параметр указан, он должен быть основан прототип функции [MSGCALLRELEASE](msgcallrelease.md) . Интерфейс **IMessage** она вызывается при счетчик ссылок объекта **IMessage**- on - **IStorage** имеет значение нуль при последнем вызове его метода **выпуска** . Если функция обратного вызова обычно используется для освобождения основной интерфейс **IStorage** . **IMessage** не пытается получить доступ к **IStorage** объект, указанный в параметре _lpStg_ после внесения обратного вызова. 
  
Некоторые клиенты или Поставщики может записывать дополнительные данные на объекте **IStorage** за пределы какие **IMessage** самого записывает при вызове метода [SaveChanges](imapiprop-savechanges.md) . Клиента или поставщика можно использовать флаг IMSG_NO_ISTG_COMMIT для предотвращения **IMessage** вызов метода OLE **IStorage::Commit** при обработке вызов **SaveChanges** ; в этом случае клиента или поставщика необходимо самого сохранить объект **IStorage** при записи дополнительных данных. Для помощи в этой реализации **IMessage** гарантирует одно имя, все substorages, которые он создает в объекте **IStorage** , начинающиеся с «__», то есть с двумя подчеркивания. Клиента или поставщика можно избежать конфликтов имен, сохранив его вложенного хранилища имена из этого пространства имен. 
  
MAPI не определяет поведение нескольких open операций, выполняемых на вложенные объекты сообщения, такие как вложения, потока или внедренных сообщений. MAPI в настоящее время позволяет вложенные объекты, открыть, чтобы открыть еще раз, но MAPI выполняет операции открытия, увеличивающееся счетчик ссылок для существующих open объекта и возврат для клиента или поставщика, который называется [IMessage::OpenAttach ](imessage-openattach.md)или метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Это означает, что запрошенный для первой операции открытия на вложенные объекты доступ доступа, для всех последующих операций открытия, независимо от того, запрошенный операциями доступ. 
  
Правильный процедуру для помещения сообщения в вложение можно вызвать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатор интерфейса IID_IMessage. **OpenProperty** в настоящее время поддерживает создание вложений сообщений доступны непосредственно в интерфейсе OLE **IStorage** , то есть, с помощью идентификатора интерфейса IID_IStorage. Чтобы разрешить простой способ поместить документ Microsoft Word в вложения без преобразования или из интерфейса OLE **IStream** поддерживается **IStorage** доступ. Тем не менее если **OpenIMsgOnIStg** передается указатель **IStorage** данные вложения, а затем выпущен объекты в том порядке **IMessage** может работать предсказуемо. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |Mfcmapi (en) использует метод **OpenIMsgOnIStg** для открытия интерфейс IMessage поверх. MSG файлов, чтобы файл может управлять с помощью интерфейса MAPI.  <br/> |
   
## <a name="see-also"></a>См. также

- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

