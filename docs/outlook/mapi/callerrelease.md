---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 69ee06ef8c8f5499dec41232d3dc7b374b15a744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808124"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**Относится к**: Outlook 
  
Определяет функцию обратного вызова, можно освободить объект данных таблицы при отпускании представлении таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Функция реализован:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
|Вызывается функция:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Параметры

 _ulCallerData_
  
> [in] Данные вызывающего сохраненных с MAPI в табличном представлении и передается **CALLERRELEASE** на основе функции обратного вызова. Данные предоставляет контекста в табличном представлении освобождения. 
    
 _lpTblData_
  
> [in] Указатель на [ITableData: IUnknown](itabledataiunknown.md) интерфейс для основной в табличном представлении освобождения, объект данных таблицы. 
    
 _lpVue_
  
> [in] Указатель на [IMAPITable: IUnknown](imapitableiunknown.md) интерфейс для освобождения, представления таблицы. Это интерфейс для объекта в таблице, возвращаемой в параметре _lppMAPITable_ метод [ITableData::HrGetView](itabledata-hrgetview.md) , создавшее этот объект к выпуску. 
    
## <a name="return-value"></a>������������ ��������

Нет 
  
## <a name="remarks"></a>Замечания

Клиентское приложение или поставщика услуг, который заполняется объект данных в таблице можно вызвать [ITableData::HrGetView](itabledata-hrgetview.md) для создания представления только для чтения, отсортированный таблицы. Вызов **HrGetView** передает указатель в функции обратного вызова **CALLERRELEASE** на основе, а также контексте сохранения с в табличном представлении. Когда счетчик ссылок в табличном представлении возвращает нулевое значение и выпуска представления, реализация **IMAPITable** вызывает функцию обратного вызова, передав контекста с помощью параметра _ulCallerData_ . 
  
Функции обратного вызова **CALLERRELEASE** на основе обычно используется для освобождения базового объекта данных в таблице и имеет для отслеживания его во время последующей обработки. 
  

