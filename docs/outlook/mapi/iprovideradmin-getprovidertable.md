---
title: Ипровидерадминжетпровидертабле
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице поставщика службы сообщений, список поставщиков служб в службе сообщений.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющая тип строк, возвращаемых в столбцах таблицы поставщика. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строковые столбцы представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, столбцы представлены в формате ANSI.
    
 _Лпптабле_
  
> вышли Указатель на указатель на таблицу поставщика.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица поставщика успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **ипровидерадмин:: жетпровидертабле** извлекает указатель на таблицу поставщика службы сообщений, таблицу, которую поддерживает MAPI, содержащую сведения о каждом поставщике услуг в службе сообщений. 
  
В отличие от таблицы поставщика, возвращенной методом [имсгсервицеадмин:: жетпровидертабле](imsgserviceadmin-getprovidertable.md) , то таблица поставщика, возвращенная **Ипровидерадмин:: жетпровидертабле** , может включать дополнительные строки, которые представляют информацию, связанную с одним или несколькими из поставщики услуг в службе сообщений. Эти дополнительные сведения добавляются к профилю с помощью ключевого слова "sections" в файле Mapisvc. INF. Когда поставщик имеет дополнительные разделы профиля, он сохраняет структуры **мапиуид** для этих разделов в свойстве **пр_сервице_екстра_уидс** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **Пр_сервице_екстра_уидс** сохраняется в разделе "профиль службы сообщений". 
  
Поставщики, которые были удалены или используются, но помечены для удаления, не включаются в таблицу поставщика. Таблицы поставщика являются статическими, что означает, что последующие добавления или удаления из службы сообщений не отражаются в таблице. 
  
Если у службы сообщений нет поставщиков, **ипровидерадмин:: жетпровидертабле** возвращает таблицу с нулевыми строками и возвращаемым значением S_OK. 
  
Установка флага МАПИ_УНИКОДЕ в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable:: куериколумнс](imapitable-querycolumns.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md) . 
  
Этот флаг также контролирует типы свойств в порядке сортировки, возвращаемом методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) . 
  
Полный список столбцов таблицы поставщик представлен в разделе [таблица поставщиков](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить строки таблицы поставщика в порядке транспорта, отсортируйте таблицу по столбцу **пр_провидер_ординал** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Чтобы получить только те строки, которые представляют поставщиков услуг (без учета лишних строк), ограничьте извлечение строками, имеющими значение ПТ_ЕРРОР в столбце **пр_ресаурце_типе** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
| Мсгсервицетабледлг. cpp  <br/> |Кмсгсервицетабледлг:: Ондисплайитем  <br/> |MFCMAPI использует метод **ипровидерадмин:: жетпровидертабле** , чтобы получить таблицу поставщиков для отображения в новом диалоговом окне.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

