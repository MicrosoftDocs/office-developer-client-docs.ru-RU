---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417408"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет подмостки.
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи подмостка для удаления.
    
 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса. Параметр _ulUIParam_ игнорируется, если флаг FOLDER_DIALOG в параметре _ulFlags._ 
    
 _lpProgress_
  
> [in] Указатель на объект progress, отображает индикатор прогресса. Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI. Параметр  _lpProgress_ игнорируется, если флаг FOLDER_DIALOG не установлен в  _ulFlags_.
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая удалением подмостков. Можно установить следующие флаги:
    
DEL_FOLDERS 
  
> Все подмостки подмостков, на которые указывает  _lpEntryID,_ должны быть удалены. 
    
DEL_MESSAGES 
  
> Все сообщения в подмостке, на которые указывает  _lpEntryID,_ должны быть удалены. 
    
FOLDER_DIALOG 
  
> Индикатор прогресса должен отображаться во время выполнения операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указанная папка успешно удалена.
    
MAPI_E_HAS_FOLDERS 
  
> Удаленный подмосток содержит подмостки, DEL_FOLDERS флаг не установлен. Подмостки не были удалены.
    
MAPI_E_HAS_MESSAGES 
  
> Удаленный подмосток содержит сообщения, а флаг DEL_MESSAGES не установлен. Подмастерье не было удалено.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов удался, но не все записи были успешно удалены. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::D eleteFolder** удаляет подмостки. По умолчанию **DeleteFolder** работает только на пустых папках, но его можно успешно использовать в непустых папках, установив два флага: DEL_FOLDERS и DEL_MESSAGES. Удаляются только пустые папки или папки, DEL_FOLDERS и DEL_MESSAGES флаги на **вызове DeleteFolder.** DEL_FOLDERS позволяет удалить все подмостки папки; DEL_MESSAGES позволяет удалить все сообщения папки. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если операция удаления включает более одной папки, выполните операцию как можно более полной для каждой папки. Иногда одна из удаленных папок не существует или была перемещена или скопирована в другом месте. Не останавливайте операцию преждевременно, если не произойдет сбой, неподконтрольный вам, например из-за потери памяти, потери дискового пространства или повреждения в хранилище сообщений.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ожидайте этих значений возврата в следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**DeleteFolder** успешно удалил каждое сообщение и подмостки.  <br/> |S_OK  <br/> |
|**DeleteFolder** не удалось успешно удалить каждое сообщение и подмостки.  <br/> |MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** не удалось выполнить.  <br/> |Любое значение ошибки, кроме MAPI_E_NOT_FOUND  <br/> |
   
Если **DeleteFolder** не удается выполнить, не думайте, что работы не было сделано. **DeleteFolder,** возможно, удалось удалить один или несколько сообщений и подмостков, прежде чем столкнуться с ошибкой. 
  
Если один или несколько подвещений не удается удалить, **DeleteFolder** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND, в зависимости от реализации поставщика магазина сообщений. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI использует метод **IMAPIFolder::D eleteFolder** для удаления папок.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

