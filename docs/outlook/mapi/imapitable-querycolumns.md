---
title: Имапитаблекуериколумнс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328884"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает список столбцов для таблицы.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, указывающих, какой набор столбцов должен быть возвращен. Можно задать следующий флаг:
    
ТБЛ_АЛЛ_КОЛУМНС 
  
> Таблица должна возвращать все доступные столбцы.
    
 _Лппроптагаррай_
  
> вышли Указатель на структуру [спроптагаррай](sproptagarray.md) , содержащую теги свойств для набора столбцов. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Набор столбцов успешно возвращен.
    
МАПИ_Е_БУСИ 
  
> Выполняется другая операция, которая не позволяет запустить операцию извлечения набора столбцов. Выполнение выполняемой операции должно быть разрешено или остановлено.
    
## <a name="remarks"></a>Комментарии

Метод **IMAPITable:: куериколумнс** можно вызвать для получения следующих компонентов: 
  
- Набор столбцов по умолчанию для таблицы.
    
- Текущий набор столбцов для таблицы, установленный при вызове метода [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) . 
    
- Полный набор столбцов для таблицы, доступные столбцы, но не обязательно входящие в текущий набор.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если не установить флаг ТБЛ_АЛЛ_КОЛУМНС, **IMAPITable:: куериколумнс** возвращает либо набор столбцов по умолчанию, либо текущий набор столбцов в зависимости от того, затронула ли таблица вызов **IMAPITable:: метода SetColumns**. **Метода SetColumns** изменяет порядок и выбор столбцов в наборе столбцов таблицы. 
  
Если установлен флаг ТБЛ_АЛЛ_КОЛУМНС, **куериколумнс** возвращает все столбцы, которые могут быть включены в набор столбцов таблицы. 
  
Освободите память для массива тегов свойств, на который указывает параметр _лппроптагаррай_ , вызвав функцию [мапифрибуффер](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Контентстаблелистктрл. cpp  <br/> |Кконтентстаблелистктрл::D Осетколумнс  <br/> |MFCMAPI использует метод **IMAPITable:: куериколумнс** , чтобы получить текущий набор столбцов для таблицы, чтобы пользователь мог ее редактировать.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

