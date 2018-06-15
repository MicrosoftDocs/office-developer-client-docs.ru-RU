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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 93578300e2520dda4a9621b05ac6a79c54eca2ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808839"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**Применимо к**: Outlook 
  
Устанавливает условия поиска для контейнера.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Parameters

 _lpRestriction_
  
> [in] Указатель на структуру [SRestriction](srestriction.md) , определяющий условия поиска. Если NULL передается в параметре _lpRestriction_ , условия поиска, которые использовались для этого контейнера наиболее часто используются еще раз. NULL не следует передавать в _lpRestriction_ для первого поиска в контейнере. 
    
 _lpContainerList_
  
> [in] Указатель на массив идентификаторов записи, которые представляют контейнеров, включаемых в поиск. Если клиент передает значение NULL в параметре _lpContainerList_ , идентификаторы записей, наиболее часто используемых для поиска в этом контейнере используются для нового поиска. Клиент не должны передавать NULL в _lpContainerList_ для первого поиска в контейнере. 
    
 _ulSearchFlags_
  
> [in] Битовая маска флаги, определяющие, как выполняется поиск. Можно задать следующие флажки:
    
BACKGROUND_SEARCH 
  
> Поиск должна запускаться с обычным приоритетом относительно других операций поиска. Этот флаг не могут задаваться одновременно флаг FOREGROUND_SEARCH.
    
FOREGROUND_SEARCH 
  
> Поиск должен выполняться с наивысший приоритет относительно других операций поиска. Этот флаг не могут задаваться одновременно флаг BACKGROUND_SEARCH.
    
NON_CONTENT_INDEXED_SEARCH
  
> Поиск не следует использовать индексирование содержимого для поиска соответствующих записей. Этот флаг допустимо только для хранилищ Exchange.
    
RECURSIVE_SEARCH 
  
> Поиск должен включать контейнеров, указанный в параметре _lpContainerList_ и всех его дочерних контейнеров. Этот флаг не могут задаваться одновременно флаг SHALLOW_SEARCH. 
    
RESTART_SEARCH 
  
> Поиск должен инициировал, если это первый вызов **SetSearchCriteria**или перезапустить Если поиска неактивных. Этот флаг не могут задаваться одновременно флаг STOP_SEARCH.
    
SHALLOW_SEARCH 
  
> Поиск должен выглядеть только в контейнерах, указанный в параметре _lpContainerList_ для соответствующих записей. Этот флаг не могут задаваться одновременно флаг RECURSIVE_SEARCH. 
    
STOP_SEARCH 
  
> Поиск должна быть остановлена. Этот флаг не могут задаваться одновременно флаг RESTART_SEARCH.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Условия поиска успешно установлены.
    
MAPI_E_TOO_COMPLEX 
  
> Поставщик услуг поддерживает заданным критериям поиска.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIContainer::SetSearchCriteria** устанавливает условия поиска для контейнера, поддерживающего поиск, обычно в папку результатов поиска. Папка результатов поиска содержит ссылки на сообщения, которые соответствуют критериям поиска; Фактические сообщения по-прежнему хранятся в исходных местах. Только уникальные данные, содержащиеся в папке результатов поиска — таблица его содержимого. В таблице содержимое папки результатов поиска имеет объединенное содержимое хранилища сообщений после применения ограничения поиска. 
  
Операция поиска работает только в этой таблице объединенные содержимого; Поиск в других папках результатов поиска. Возвращает результаты поиска только сообщения, соответствующие критериям поиска; Иерархия папок не возвращаются.
  
Управление возвращается клиенту после завершения поиска.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Контейнеры адресной книги устанавливать условия поиска с применением ограничений на их содержимое таблицы. Дополнительные сведения о критерии поиска и адресной книги контейнеров см [Реализация расширенного поиска](implementing-advanced-searching.md).
  
Следует поддержки open, копирование, перемещение и удаления сообщений в папках результатов поиска, а не к самой папке результатов поиска. Не разрешать сообщения, чтобы быть созданы в рамках или скопирован в папку результатов поиска. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы найти получателей сообщения, задайте _lpRestriction_ для указания на ограничений вложенные объекты с член **ulSubObject** в структуре [SSubRestriction](ssubrestriction.md) , задайте значение **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Поиск вложений, укажите элемент **ulSubObject** в **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Укажите элемент **lpRes** для указания на ограничение свойство, которое описывает условия поиска для получателей или вложения. 
  
Например для поиска файлов вложений, которые имеют расширение .mss, задайте **ulSubObject** **PR_MESSAGE_ATTACHMENTS** и **lpRes** для свойства ограничение, которое соответствует **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) с. mss.
  
Установка флага FOREGROUND_SEARCH с помощью параметра _ulSearchFlags_ может привести к снижению производительности системы. 
  
Чтобы изменить параметры поиска для поиска в уже начатую можно использовать **SetSearchCriteria** . Можно указать новые ограничения, новые списки папок для поиска и новый приоритет поиска, такие как обновление поиска более высокий приоритет. Изменения в приоритет поиска не существующий поиск для перезапуска, но можно другие изменения в условия поиска. 
  
После завершения работы с помощью папки результатов поиска, можно удалить папку или сообщите его остаются открытыми для дальнейшего использования. Если удалить папку результатов поиска, только ссылки сообщения будут удалены. Фактические сообщения остаются в родительских папок. 
  
Дополнительные сведения о папках результатов поиска можно [Папок поиска MAPI](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |Mfcmapi (en) использует метод **IMAPIContainer::SetSearchCriteria** для записи условия поиска для папки после измененный пользователя.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[SSubRestriction](ssubrestriction.md)
  
[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

