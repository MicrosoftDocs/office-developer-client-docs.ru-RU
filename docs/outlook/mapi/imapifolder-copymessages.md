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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _lpMsgList_
  
> [in] Указатель на массив структур [ENTRYLIST,](entrylist.md) которые определяют сообщения или сообщения для копирования или перемещения. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к папке назначения, указываемой параметром _lpDestFolder._ Передача NULL приводит к возвращению поставщиком услуг интерфейса стандартной папки [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Клиенты должны пройти NULL. Другие звонители могут установить параметр  _lpInterface_ для IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Указатель на открытую папку для получения скопированные или перенесенные сообщения.
    
 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом. Параметр _ulUIParam_ игнорируется, если клиент не задает флаг MESSAGE_DIALOG в _параметре ulFlags_ и не передает NULL в _параметре lpProgress._ 
    
 _lpProgress_
  
> [in] Указатель на объект progress, отображает индикатор прогресса. Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI. Параметр  _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в  _ulFlags_.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют выполнение операции копирования или перемещения. Можно установить следующие флаги:
    
MAPI_DECLINE_OK 
  
> Информирует поставщика магазина сообщений о немедленном возвращении MAPI_E_DECLINE_COPY, если он реализует метод **IMAPIFolder::CopyMessages,** назвав [IMAPISupport объекта поддержки::D oCopyTo](imapisupport-docopyto.md) или [IMAPISupport::D oCopyProps.](imapisupport-docopyprops.md) 
    
MESSAGE_DIALOG 
  
> Отображает индикатор прогресса по мере выполнения операции.
    
MESSAGE_MOVE 
  
> Сообщение или сообщения должны быть перемещены вместо копирования. Если MESSAGE_MOVE не установлено, сообщения копируется.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение или сообщения успешно копируется или перемещается.
    
MAPI_E_DECLINE_COPY 
  
> Поставщик реализует этот метод, вызывая метод объекта поддержки, и вызыватель передал флаг MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов удался, но не все записи были успешно скопированы или перемещены. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::CopyMessages** копирует или перемещает сообщения в другую папку. 
  
Сообщения, которые открываются с разрешения на чтение или записи, могут быть перемещены или скопированы. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вы копируете сообщения в другой магазин сообщений без использования метода [IMAPISupport::CopyMessages,](imapisupport-copymessages.md) сначала необходимо вызвать [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) с набором флага GENERATE_RECEIPT_ONLY. Хранилище сообщений для получения не несет ответственности за создание отчетов о считывке скопированные или перенесенные сообщения. Если вы вызываете **IMAPISupport::CopyMessages** для реализации **IMAPIFolder::CopyMessages,** не вызывай **SetReadFlags;** MAPI будет вызывать его. 
  
Реализация может перемещать или копировать сообщения в любом порядке и создавать отчеты о состоянии чтения в любом порядке. То есть можно завершить копирование сообщений, прежде чем создавать какие-либо отчеты о состоянии чтения или отправлять отчеты перед началом операции копирования. Однако отчеты о считыве должны быть отправлены для копирования всех сообщений независимо от того, является ли копия успешной.
  
Если операция копирования или перемещения включает несколько сообщений, выполните операцию максимально полностью. Не останавливайте операцию преждевременно, если не произойдет сбой, неподконтрольный вам, например из-за потери памяти, потери дискового пространства или повреждения в хранилище сообщений.
  
Попробуйте сохранить идентификаторы записей в операциях перемещения или копирования. Кроме того, необходимо сохранить идентификаторы записей, хотя это и не требуется.
  
Отправка уведомлений при движении или копировании сообщений таким образом, чтобы клиенты были уведомлены о том, что их вызовы в [методы IMAPIProp::SaveChanges](imapiprop-savechanges.md) могут не сбой. 
  
Не включай состояние сообщения в операцию копирования или перемещения. Перемещение или копирование состояния сообщения значительно влияет на производительность.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Используйте **IMAPIFolder::CopyMessages** для заполнения папок результатов поиска, где сообщения часто группируются по родительской папке. 
  
Ожидайте этих значений возврата в следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** успешно копирует или перемещает каждое сообщение.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** не удалось успешно скопировать или переместить каждое сообщение.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** не удалось выполнить.  <br/> |Любое значение ошибки  <br/> |
   
Когда **IMAPIFolder::CopyMessages** не удается выполнить, не предполагать, что работа не была сделана. **IMAPIFolder::CopyMessages,** возможно, удалось скопировать или переместить одно или несколько сообщений, прежде чем столкнуться с ошибкой. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

