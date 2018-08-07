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
ms.openlocfilehash: 2ad57b91a1b9d06ab8284fa53c283d17e4eb5613
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809544"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Относится к**: Outlook 
  
Предоставляет доступ к таблице поставщика службы сообщений, список поставщиков услуг службы сообщений.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип строк, возвращаемых в столбцов таблицы поставщика. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Столбцы строку, в формате Юникод. Если флаг MAPI_UNICODE не установлен, столбцы представлены в формате ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель в таблице поставщика.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице поставщика успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IProviderAdmin::GetProviderTable** получает указатель на таблице поставщика службы сообщений, таблицы, которая поддерживает MAPI, содержащий сведения о каждой поставщика услуг службы сообщений. 
  
В отличие от поставщика таблицы, возвращенный методом [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) в таблице поставщика, возвращаемые **IProviderAdmin::GetProviderTable** может включать дополнительные строки, которые представляют сведения, связанные с одним или несколькими из Поставщики услуг службы сообщений. Эти дополнительные данные добавляется к профилю ключевое слово «Раздела» файла Mapisvc.inf. Поставщик имеет разделах дополнительных профилей, сохраняется структур **MAPIUID** для этих разделов в свойстве **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** сохраняется в разделе сообщения службы профилей. 
  
Поставщики, которые были удалены, или используется, но помечены для удаления, не включаются в таблице поставщика. Поставщик таблиц являются статическими, что означает, что последующие дополнения или удалений из службы сообщений, не отражаются в таблице. 
  
Если у службы сообщение нет поставщиков, **IProviderAdmin::GetProviderTable** возвращает таблицу с нуля строк и возвращаемое значение S_OK. 
  
Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) . 
  
Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
Полный список столбцов в таблице поставщика в разделе [Поставщик в таблице](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для получения строк таблицы поставщика в порядке транспорта, сортировку таблицы в столбце **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Чтобы получить только те строки, представляющие поставщиков услуг (не включая любые дополнительные строки), ограничение на извлечение строк со значением PT_ERROR в столбце **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |Mfcmapi (en) использует метод **IProviderAdmin::GetProviderTable** для получения таблицы поставщиков для отображения в диалоговом окне новый.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

