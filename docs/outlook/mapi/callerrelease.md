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
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408728"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет функцию вызова, которая может освободить объект данных таблицы при выпуске представления таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Определяемая функция, реализованная в:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Определяемая функция, вызванная:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Параметры

 _ulCallerData_
  
> [in] Данные вызываемого звонка, сохраненные с помощью MAPI в представлении таблицы и переданные функции вызова на основе **CALLERRELEASE.** Данные предоставляют контекст о представлении таблицы, которая будет отпущена. 
    
 _lpTblData_
  
> [in] Указатель на [интерфейс ITableData : интерфейс IUnknown](itabledataiunknown.md) для объекта данных таблицы, который находится в окне выпускаемого представления таблицы. 
    
 _lpVue_
  
> [in] Указатель на [интерфейс IMAPITable : интерфейс IUnknown](imapitableiunknown.md) для выпуска представления таблицы. Это интерфейс для объекта таблицы, возвращаемого в  _параметре lppMAPITable_ метода [ITableData::HrGetView,](itabledata-hrgetview.md) который создал объект для освобождения. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет 
  
## <a name="remarks"></a>Примечания

Клиентские приложения или поставщик службы, заполнив объект данных таблицы, могут вызвать [ITableData::HrGetView,](itabledata-hrgetview.md) чтобы создать представление таблицы только для чтения. Вызов **HrGetView** передает указатель функции вызова на основе **CALLERRELEASE,** а также контекст, который необходимо сохранить в представлении таблицы. Когда отсчет представления таблицы возвращается к нулю и представление отпущено, реализация **IMAPITable** вызывает функцию обратного вызова, передавая контекст в _параметре ulCallerData._ 
  
Функция callback на основе **CALLERRELEASE** часто используется для освобождения объекта данных таблицы, который не должен отслеживаться во время последующей обработки. 
  

