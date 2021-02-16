---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424457"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует или перемещает одно или несколько сообщений.
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpMsgList_
  
> [in] Указатель на массив структур [ENTRYLIST,](entrylist.md) которые определяют сообщения, которые необходимо скопировать или переместить. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к папке назначения, на которую указывает параметр _lpDestFolder._ Передача NULL приводит к возвращению поставщиком службы стандартного интерфейса папки [IMAPIFolder : IMAPIContainer.](imapifolderimapicontainer.md) Клиенты должны передавать NULL. Другие вызыватели могут установить для  _параметра lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Указатель на открытую папку для получения скопированные или перемещенные сообщения.
    
 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows this method displays. Параметр _ulUIParam_ игнорируется, если клиент не устанавливает флаг MESSAGE_DIALOG в _параметре ulFlags_ и не передает NULL в _параметре lpProgress._ 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI. Параметр _lpProgress_ игнорируется, если MESSAGE_DIALOG флага в _ulFlags._
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет выполнением операции копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DECLINE_OK 
  
> Сообщает поставщику хранения сообщений о немедленном возвращении MAPI_E_DECLINE_COPY, если он реализует **метод IMAPIFolder::CopyMessages,** вызывая метод [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) или [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) объекта поддержки. 
    
MESSAGE_DIALOG 
  
> Отображает индикатор хода выполнения операции.
    
MESSAGE_MOVE 
  
> Вместо копирования сообщения или сообщения перемещаются. Если MESSAGE_MOVE не установлен, сообщения копируется.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщения или сообщения успешно скопированы или перемещены.
    
MAPI_E_DECLINE_COPY 
  
> Поставщик реализует этот метод, вызывая метод объекта поддержки, и вызываемая стороны передает флаг MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов был успешным, но не все записи были успешно скопированы или перемещены. При возвращении этого предупреждения вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.** Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::CopyMessages** копирует или перемещает сообщения в другую папку. 
  
Сообщения, которые открываются с разрешением на чтение и записи, могут быть перемещены или скопированы. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

При копировании сообщений в другое хранилище сообщений без использования метода [IMAPISupport::CopyMessages](imapisupport-copymessages.md) необходимо сначала вызвать [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) с установленным флагом GENERATE_RECEIPT_ONLY. Хранилище принимающих сообщений не отвечает за создание отчетов о прочтение скопированные или перемещенные сообщения. Если вы вызываете **IMAPISupport::CopyMessages** для реализации **IMAPIFolder::CopyMessages,** не **вызываем SetReadFlags;** MAPI будет вызывать его. 
  
Реализация может перемещать или копировать сообщения в любом порядке и создавать отчеты о состоянии чтения в любом порядке. То есть вы можете завершить копирование сообщений перед созданием отчетов о состоянии чтения или отправить отчеты до того, как реализация начнет операцию копирования. Однако для копирования всех сообщений следует отправлять отчеты о прочтеных сообщениях независимо от того, была ли копия успешной.
  
Если операция копирования или перемещения включает несколько сообщений, выполните операцию как можно точнее. Не останавливайте операцию раньше времени, если не произойдет сбой, который находится вне вашего контроля, например, если недостаточно памяти, недостаточно места на диске или не будет повреждения в хранилище сообщений.
  
Старайтесь поддерживать идентификаторы записей при операциях перемещения или копирования. Также следует сохранить идентификаторы записей, хотя это и не требуется.
  
Отправка уведомлений при перемещения или копировании сообщений таким образом, чтобы клиенты были предварительно уведомлены о том, что их вызовы методов [IMAPIProp::SaveChanges](imapiprop-savechanges.md) могут не удастся. 
  
Не включаем состояние сообщения в операцию копирования или перемещения. Перемещение или копирование состояния сообщения значительно влияет на производительность.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Используйте **IMAPIFolder::CopyMessages** для заполнения папок результатов поиска, где сообщения часто группируют по родительской папке. 
  
Эти возвращаемые значения следует ожидать при следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** has successfully copied or moved every message.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** не удалось успешно скопировать или переместить каждое сообщение.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|Не удалось завершить **IMAPIFolder::CopyMessages.**  <br/> |Любое значение ошибки  <br/> |
   
Если **IMAPIFolder::CopyMessages** не удается завершить, не предполагать, что никаких работ не было сделано. **Возможно, IMAPIFolder::CopyMessages** мог скопировать или переместить одно или несколько сообщений, прежде чем столкнуться с ошибкой. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

