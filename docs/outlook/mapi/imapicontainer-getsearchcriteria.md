---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4ca565f97851a2efe2f3279f062f6ea89a4c6326
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579965"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает параметры поиска для контейнера.
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип строк, переданное. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _lppRestriction_
  
> [out] Указатель на указатель на структуру [SRestriction](srestriction.md) , определяющий условия поиска. Если клиентское приложение передает значение NULL в параметре _lppRestriction_ , **GetSearchCriteria** не возвращает структуру **SRestriction** . 
    
 _lppContainerList_
  
> [out] Указатель на указатель на массив идентификаторов записи, которые представляют контейнеров, включаемых в поиск. Если клиент передает значение NULL в параметре _lppContainerList_ , **GetSearchCriteria** не возвращает массив идентификаторов запись. 
    
 _lpulSearchState_
  
> [out] Указатель на битовой маски флагов, используемых для указания текущего состояния поиска. Если клиент передает значение NULL в параметре _lpulSearchState_ , **GetSearchCriteria** Возвращает флаги не. Можно задать следующие флажки: 
    
SEARCH_FOREGROUND 
  
> Поиск должен выполняться с наивысший приоритет относительно других операций поиска. Если этот флаг не установлен, с обычным приоритетом относительно других операций поиска выполняется поиск.
    
SEARCH_REBUILD 
  
> Поиск — в режиме высокой загрузкой ЦП операции, чтобы найти сообщения, соответствующие критериям. Если этот флаг не установлен, окончена высокой загрузкой ЦП частью операции поиска. Этот флаг имеет значение только в том случае, если поиск является активным (то есть, если установлен флаг SEARCH_RUNNING).
    
SEARCH_RECURSIVE 
  
> Поиск в заданных контейнеров и всех их дочерних контейнеров для соответствующих записей. Если этот флаг не установлен, только контейнеры, явно включены в последнем вызове метода [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) которых осуществляется поиск. 
    
SEARCH_RUNNING 
  
> Поиск является активной и контейнера содержимое таблицы обновляется для отражения изменений в хранилище сообщений или адресная книга. Если этот флаг не установлен, поиска неактивных и статического содержимого таблицы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Условия поиска успешно был получен.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
MAPI_E_NOT_INITIALIZED 
  
> Условия поиска никогда не были настроены для контейнера.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIContainer::GetSearchCriteria** получает условия поиска для контейнера, поддерживающего поиск, обычно в папку результатов поиска. Создание условия поиска, вызвав метод **IMAPIContainer::SetSearchCriteria** контейнера. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Контейнеры адресной книги может потребоваться поддержка **GetSearchCriteria** только в том случае, если они предоставляют возможности расширенного поиска, связанного со свойством **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Дополнительные сведения о том, как реализовать функцию расширенного поиска для контейнеров адресной книги, можно [Реализация расширенный поиск](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После завершения структуры данных, на который указывает параметры _lppRestriction_ и _lppContainerList_ вызов [MAPIFreeBuffer](mapifreebuffer.md) один раз для каждого структуры нужно освободить. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |Mfcmapi (en) использует метод **IMAPIContainer::GetSearchCriteria** для получения условия поиска из папки для отображения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

