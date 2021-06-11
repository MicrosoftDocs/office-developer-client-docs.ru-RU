---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434475"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице поставщиков сообщений, списку поставщиков услуг в службе сообщений.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Немного флагов, которые контролируют тип строк, возвращаемых в столбцах таблицы поставщика. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Столбцы строк находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, столбцы находятся в формате ANSI.
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблицу поставщика.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица поставщика успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IProviderAdmin::GetProviderTable** извлекает указатель в таблицу поставщика службы сообщений, таблицу, которую поддерживает MAPI, которая содержит сведения о каждом поставщике услуг в службе сообщений. 
  
В отличие от таблицы поставщиков, возвращаемой методом [IMsgServiceAdmin:::GetProviderTable,](imsgserviceadmin-getprovidertable.md) таблица поставщиков, возвращенная **IProviderAdmin::GetProviderTable,** может включать дополнительные строки, которые представляют сведения, связанные с одним или более поставщиками услуг в службе сообщений. Эта дополнительная информация добавляется в профиль с помощью ключевого слова "Разделы" файла Mapisvc.inf. Если у поставщика есть дополнительные разделы профилей, он сохраняет структуры **MAPIUID** для этих разделов в **свойстве** [PR_SERVICE_EXTRA_UIDS (PidTagServiceExtraUids).](pidtagserviceextrauids-canonical-property.md) **PR_SERVICE_EXTRA_UIDS** сохранена в разделе профиль службы сообщений. 
  
Поставщики, которые были удалены или используются, но помечены для удаления, не включены в таблицу поставщиков. Таблицы поставщиков являются статичными, что означает, что последующие добавления или удаления из службы сообщений не отражаются в таблице. 
  
Если служба сообщений не имеет поставщиков, **IProviderAdmin::GetProviderTable** возвращает таблицу с нулевыми строками и значением S_OK возвращается. 
  
Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых из методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md) 
  
Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
Полный список столбцов в таблице поставщиков см. в [статье Provider Table.](provider-tables.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить строки таблицы поставщика в порядке транспорта, **сортировать таблицу** по столбце [PR_PROVIDER_ORDINAL (PidTagProviderOrdinal).](pidtagproviderordinal-canonical-property.md) 
  
Чтобы получить только те строки, которые представляют поставщиков услуг (без дополнительных строк), ограничьте извлечение строками, которые имеют значение PT_ERROR в столбце **PR_RESOURCE_TYPE** [(PidTagResourceType).](pidtagresourcetype-canonical-property.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI использует **метод IProviderAdmin::GetProviderTable** для получения таблицы поставщиков для отрисовки в новом диалоговом окне.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

