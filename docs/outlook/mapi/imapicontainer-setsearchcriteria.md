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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Устанавливает условия поиска для контейнера.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Параметры

 _lpRestriction_
  
> [in] Указатель на структуру [SRestriction,](srestriction.md) которая определяет условия поиска. Если в параметре  _lpRestriction_ передается NULL, критерии поиска, которые использовались недавно для этого контейнера, используются повторно. NULL не следует передавать в  _lpRestriction_ для первого поиска в контейнере. 
    
 _lpContainerList_
  
> [in] Указатель на массив идентификаторов записей, которые представляют контейнеры, которые необходимо включить в поиск. Если клиент передает NULL в  _параметре lpContainerList,_ идентификаторы записей, использованные недавно для поиска в этом контейнере, используются для нового поиска. Клиент не должен передавать NULL в  _lpContainerList_ для первого поиска в контейнере. 
    
 _ulSearchFlags_
  
> [in] Битоваяmas флагов, которые контролируют выполнение поиска. Можно установить следующие флаги:
    
BACKGROUND_SEARCH 
  
> Поиск должен запускаться с обычным приоритетом относительно других поисковых запросов. Этот флаг нельзя установить одновременно с флагом FOREGROUND_SEARCH флага.
    
FOREGROUND_SEARCH 
  
> Поиск должен работать с высоким приоритетом относительно других поисковых запросов. Этот флаг нельзя установить одновременно с флагом BACKGROUND_SEARCH флага.
    
NON_CONTENT_INDEXED_SEARCH
  
> Поиск не должен использовать индексацию контента для поиска совпадающих записей. Этот флаг действителен только для хранилищ Exchange.
    
RECURSIVE_SEARCH 
  
> Поиск должен включать контейнеры, указанные в параметре  _lpContainerList,_ и все их потомки. Этот флаг нельзя установить одновременно с флагом SHALLOW_SEARCH флага. 
    
RESTART_SEARCH 
  
> Поиск следует инициировать, если это первый вызов **SetSearchCriteria,** или перезапустить, если поиск неактивный. Этот флаг нельзя установить одновременно с флагом STOP_SEARCH флага.
    
SHALLOW_SEARCH 
  
> Поиск должен выглядеть только в контейнерах, указанных в параметре  _lpContainerList_ для совпадающих записей. Этот флаг нельзя установить одновременно с флагом RECURSIVE_SEARCH флага. 
    
STOP_SEARCH 
  
> Поиск должен быть остановлен. Этот флаг нельзя установить одновременно с флагом RESTART_SEARCH флага.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Критерии поиска успешно установлены.
    
MAPI_E_TOO_COMPLEX 
  
> Поставщик услуг не поддерживает указанные условия поиска.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer::SetSearchCriteria** устанавливает условия поиска для контейнера, который поддерживает поиск, как правило, папку результатов поиска. Папка результатов поиска содержит ссылки на сообщения, которые соответствуют условиям поиска; фактические сообщения по-прежнему хранятся в их исходных расположениях. Единственные уникальные данные, содержащиеся в папке результатов поиска, — это ее таблица содержимого. Таблица содержимого папки результатов поиска имеет объединенную информацию о хранилище сообщений после примененного ограничения поиска. 
  
Операция поиска работает только в этой объединенной таблице содержимого; он не будет искать другие папки результатов поиска. Результаты поиска возвращают только сообщения, которые соответствуют условиям поиска; Иерархия папок не возвращается.
  
После завершения поиска клиенту возвращается управление.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Контейнеры адресных книг устанавливают условия поиска, применяя ограничения к своим таблицам содержимого. Дополнительные сведения о критериях поиска и контейнерах адресной книги см. в этой [теме.](implementing-advanced-searching.md)
  
Операции открытия, копирования, перемещения и удаления сообщений в папках результатов поиска должны поддерживаться, а не в самой папке результатов поиска. Не разрешать создавать сообщения в папке результатов поиска или копировать их в нее. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы найти получателей сообщений, установите _для lpRestriction_ ограничение подобъекта с членом **ulSubObject** в структуре [SSubRestriction,](ssubrestriction.md) задав для **него** PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients).](pidtagmessagerecipients-canonical-property.md) Чтобы найти вложения, установите для члена **ulSubObject** PR_MESSAGE_ATTACHMENTS **(** [PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md) Установите для **члена lpRes** ограничение свойства, которое описывает условия поиска для получателей или вложений. 
  
Например, чтобы найти вложения с расширением MSS, установите для **ulSubObject** PR_MESSAGE_ATTACHMENTS и **lpRes** ограничение свойства, которое соответствует **PR_ATTACH_EXTENSION** ([PidTagAttachExtension)](pidtagattachextension-canonical-property.md)с .mss. 
  
Установка флага FOREGROUND_SEARCH в параметре  _ulSearchFlags_ может привести к снижению производительности системы. 
  
С помощью **SetSearchCriteria** можно изменить условия поиска, которые уже ведутся. Можно указать новые ограничения, новые списки папок для поиска и новый приоритет поиска, например обновление поиска до более высокого приоритета. Изменения приоритета поиска не приводят к перезапуску существующего поиска, но другие изменения в критериях поиска могут быть. 
  
Когда вы используете папку результатов поиска, вы можете удалить ее или позволить ей оставаться открытой для использования в дальнейшем. Если удалить папку результатов поиска, удаляются только ссылки на сообщения. Фактические сообщения остаются в родительских папках. 
  
Дополнительные сведения о папках результатов поиска см. в папках поиска [MAPI.](mapi-search-folders.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI использует метод **IMAPIContainer::SetSearchCriteria** для написания критериев поиска для папки после ее изменения пользователем.  <br/> |
   
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

