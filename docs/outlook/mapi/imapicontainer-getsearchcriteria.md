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
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412025"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает условия поиска для контейнера.
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом переданных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _lppRestriction_
  
> [out] Указатель на указатель на [структуру SRestriction,](srestriction.md) которая определяет условия поиска. Если клиентские приложения проходят NULL в _параметре lppRestriction,_ **GetSearchCriteria** не возвращает **структуру SRestriction.** 
    
 _lppContainerList_
  
> [out] Указатель на указатель на массив идентификаторов записей, которые представляют контейнеры, которые необходимо включить в поиск. Если клиент передает NULL в  _параметре lppContainerList,_ **GetSearchCriteria** не возвращает массив идентификаторов записей. 
    
 _lpulSearchState_
  
> [out] Указатель на битовуюметку флагов, которая указывает текущее состояние поиска. Если клиент передает NULL в  _параметре lpulSearchState,_ **GetSearchCriteria** не возвращает флаги. Можно установить следующие флаги: 
    
SEARCH_FOREGROUND 
  
> Поиск должен работать с высоким приоритетом относительно других поисковых запросов. Если этот флаг не установлен, поиск выполняется с обычным приоритетом относительно других поисковых запросов.
    
SEARCH_REBUILD 
  
> Поиск находится в режиме интенсивной работы ЦП и пытается найти сообщения, которые соответствуют условиям. Если этот флаг не установлен, интенсивное ЦП часть операции поиска будет установлена. Этот флаг имеет значение, только если поиск активен (то есть если SEARCH_RUNNING установлен).
    
SEARCH_RECURSIVE 
  
> Поиск ищет в указанных контейнерах и всех их потомков контейнерах для поиска совпадающих записей. Если этот флаг не установлен, поиск ведется только в контейнерах, явно включенных в последний вызов метода [IMAPIContainer::SetSearchCriteria.](imapicontainer-setsearchcriteria.md) 
    
SEARCH_RUNNING 
  
> Поиск активен, и таблица содержимого контейнера обновляется с учетом изменений в хранилище сообщений или адресной книге. Если этот флаг не установлен, поиск неактивный, а таблица содержимого является статической.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Критерии поиска успешно получены.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
MAPI_E_NOT_INITIALIZED 
  
> Условия поиска для контейнера не были установлены.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer::GetSearchCriteria** получает условия поиска для контейнера, который поддерживает поиск, обычно папку результатов поиска. Критерии поиска создаются путем вызова метода **IMAPIContainer::SetSearchCriteria контейнера.** 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Контейнерам адресной книги может потребоваться поддержка **GetSearchCriteria,** только если они предоставляют расширенные возможности поиска, связанные со свойством **PR_SEARCH** ([PidTagSearch).](pidtagsearch-canonical-property.md) Дополнительные сведения о реализации функции расширенный поиск для контейнеров адресной книги см. в [реализации функции "Расширенный поиск".](implementing-advanced-searching.md)
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Завершив работу со структурами данных, на которые указывают параметры  _lppRestriction_ и  _lppContainerList,_ вызовите [MAPIFreeBuffer](mapifreebuffer.md) один раз, чтобы освободить каждую структуру. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI использует метод **IMAPIContainer::GetSearchCriteria** для получения критериев поиска из папки для отображения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

