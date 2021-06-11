---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427201"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устанавливает критерии поиска для контейнера.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Parameters

 _lpRestriction_
  
> [in] Указатель на [структуру SRestriction,](srestriction.md) определяемую критериями поиска. Если NULL передается в  _параметре lpRestriction,_ снова используются критерии поиска, которые использовались совсем недавно для этого контейнера. NULL не следует передавать в  _lpRestriction_ для первого поиска в контейнере. 
    
 _lpContainerList_
  
> [in] Указатель на массив идентификаторов записей, которые представляют контейнеры, которые будут включены в поиск. Если клиент передает NULL в  _параметре lpContainerList,_ идентификаторы записей, используемые совсем недавно для поиска этого контейнера, используются для нового поиска. Клиент не должен передавать NULL в  _lpContainerList_ для первого поиска в контейнере. 
    
 _ulSearchFlags_
  
> [in] Немного флагов, которые контролируют выполнение поиска. Можно установить следующие флаги:
    
BACKGROUND_SEARCH 
  
> Поиск должен работать в обычном приоритете по сравнению с другими поисками. Этот флаг нельзя установить одновременно с FOREGROUND_SEARCH флагом.
    
FOREGROUND_SEARCH 
  
> Поиск должен работать с высоким приоритетом по сравнению с другими поисками. Этот флаг не может быть установлен одновременно с BACKGROUND_SEARCH флагом.
    
NON_CONTENT_INDEXED_SEARCH
  
> Поиск не должен использовать индексацию контента для поиска совпадающих записей. Этот флаг действителен только для Exchange магазинов.
    
RECURSIVE_SEARCH 
  
> Поиск должен включать контейнеры, указанные в параметре  _lpContainerList,_ и все их детские контейнеры. Этот флаг нельзя установить одновременно с SHALLOW_SEARCH флагом. 
    
RESTART_SEARCH 
  
> Поиск следует начать, если это первый вызов **в SetSearchCriteria,** или перезапустить, если поиск неактивный. Этот флаг нельзя установить одновременно с STOP_SEARCH флагом.
    
SHALLOW_SEARCH 
  
> Поиск должен искаться только в контейнерах, указанных в параметре  _lpContainerList_ для совпадения записей. Этот флаг нельзя установить одновременно с RECURSIVE_SEARCH флагом. 
    
STOP_SEARCH 
  
> Поиск должен быть остановлен. Этот флаг не может быть установлен одновременно с RESTART_SEARCH флагом.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Критерии поиска были успешно установлены.
    
MAPI_E_TOO_COMPLEX 
  
> Поставщик услуг не поддерживает указанные критерии поиска.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer::SetSearchCriteria** устанавливает критерии поиска для контейнера, поддерживающем поиск, как правило, папки результатов поиска. Папка результатов поиска содержит ссылки на сообщения, которые соответствуют критериям поиска; фактические сообщения по-прежнему хранятся в исходных расположениях. Единственные уникальные данные, содержащиеся в папке результатов поиска, — это ее таблица контента. В таблице содержимого папки результатов поиска после примененного ограничения поиска слито содержимое магазина сообщений. 
  
Операция поиска работает только в этой объединенной таблице содержимого; он не будет искать в других папках результатов поиска. Результаты поиска возвращают только сообщения, которые соответствуют критериям поиска; иерархия папок не возвращается.
  
Управление возвращается клиенту по завершению поиска.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Контейнеры адресных книг устанавливают критерии поиска, применяя ограничения к таблицам контента. Дополнительные сведения о критериях поиска и контейнерах адресной книги см. в книге [Implementing Advanced Search.](implementing-advanced-searching.md)
  
Необходимо поддерживать открытие, копирование, перемещение и удаление операций на сообщениях в папках результатов поиска, а не в самой папке результатов поиска. Не допускайте создания сообщений в папке результатов поиска или их копирования. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы найти получателей сообщений, установите _lpRestriction,_ чтобы указать на ограничение субобъекта с членом **ulSubObject** в структуре [SSubRestriction,](ssubrestriction.md) задаваемой PR_MESSAGE_RECIPIENTS [(PidTagMessageRecipients).](pidtagmessagerecipients-canonical-property.md)  Чтобы найти вложения, установите **члену ulSubObject** PR_MESSAGE_ATTACHMENTS [(PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md)  Установите **члену lpRes** указать на ограничение свойств, которое описывает критерии поиска для получателей или вложений. 
  
Например, чтобы найти вложения файлов с расширением .mss, установите **ulSubObject** **для PR_MESSAGE_ATTACHMENTS** и **lpRes** к ограничению свойств, которое соответствует PR_ATTACH_EXTENSION [(PidTagAttachExtension)](pidtagattachextension-canonical-property.md)с .mss. 
  
Установка флага FOREGROUND_SEARCH в  _параметре ulSearchFlags_ может привести к снижению производительности системы. 
  
Вы можете использовать **SetSearchCriteria,** чтобы изменить критерии поиска уже в процессе поиска. Можно указать новые ограничения, новые списки папок для поиска и новый приоритет поиска, например обновление поиска до более высокого приоритета. Изменения приоритета поиска не приводят к перезапуску существующего поиска, но другие изменения в критериях поиска могут быть. 
  
Когда вы используете папку результатов поиска, вы можете удалить папку или позволить ей оставаться открытой для более позднего использования. Если вы удалите папку результатов поиска, удаляются только ссылки на сообщения. Фактические сообщения остаются в родительских папках. 
  
Дополнительные сведения о папках результатов поиска см. в [папках поиска MAPI.](mapi-search-folders.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI использует метод **IMAPIContainer::SetSearchCriteria** для записи критериев поиска для папки после ее редактирования пользователем.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[SSubRestriction](ssubrestriction.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

