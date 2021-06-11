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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает критерии поиска для контейнера.
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом переданных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 _lppRestriction_
  
> [вышел] Указатель на указатель на [структуру SRestriction,](srestriction.md) определяемую критериями поиска. Если клиентное приложение передает NULL в _параметре lppRestriction,_ **GetSearchCriteria** не возвращает **структуру SRestriction.** 
    
 _lppContainerList_
  
> [вышел] Указатель на указатель на массив идентификаторов записей, которые представляют контейнеры, которые будут включены в поиск. Если клиент передает NULL в  _параметре lppContainerList,_ **GetSearchCriteria** не возвращает массив идентификаторов записи. 
    
 _lpulSearchState_
  
> [вышел] Указатель на битмаску флагов, используемых для указать текущее состояние поиска. Если клиент передает NULL в  _параметре lpulSearchState,_ **GetSearchCriteria** не возвращает флаги. Можно установить следующие флаги: 
    
SEARCH_FOREGROUND 
  
> Поиск должен работать с высоким приоритетом по сравнению с другими поисками. Если этот флаг не установлен, поиск выполняется в обычном приоритете по сравнению с другими поисками.
    
SEARCH_REBUILD 
  
> Поиск находится в режиме интенсивной работы ЦП, пытаясь найти сообщения, которые соответствуют критериям. Если этот флаг не заданной, то интенсивная для ЦП часть операции поиска будет отсвечена. Этот флаг имеет значение только в том случае, если поиск активен (то есть если SEARCH_RUNNING заданной).
    
SEARCH_RECURSIVE 
  
> Поиск ищется в указанных контейнерах и всех их детских контейнерах для совпадающих записей. Если этот флаг не установлен, в поиске находятся только контейнеры, явно включенные в последний вызов метода [IMAPIContainer::SetSearchCriteria.](imapicontainer-setsearchcriteria.md) 
    
SEARCH_RUNNING 
  
> Поиск активен, а таблица содержимого контейнера обновляется с учетом изменений в хранилище сообщений или адресной книге. Если этот флаг не установлен, поиск неактивный, а таблица содержимого статична.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Критерии поиска были успешно получены.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
MAPI_E_NOT_INITIALIZED 
  
> Для контейнера никогда не были установлены критерии поиска.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer::GetSearchCriteria** получает критерии поиска для контейнера, поддерживающем поиск, как правило, папки результатов поиска. Вы создаете критерии поиска, вызывая метод **IMAPIContainer::SetSearchCriteria.** 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Контейнеры адресных книг могут нуждаться в поддержке **GetSearchCriteria** только в том случае, если они предоставляют расширенные возможности поиска, связанные с **свойством PR_SEARCH** [(PidTagSearch).](pidtagsearch-canonical-property.md) Дополнительные сведения о том, как реализовать функцию расширенный поиск для контейнеров адресных книг, см. в книге [Implementing Advanced Search.](implementing-advanced-searching.md)
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда вы закончите работу со структурами данных, на которые указывают параметры  _lppRestriction_ и  _lppContainerList,_ позвоните [ПО MAPIFreeBuffer](mapifreebuffer.md) один раз для выпуска каждой структуры. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI использует **метод IMAPIContainer::GetSearchCriteria** для получения критериев поиска в папке для отображения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

