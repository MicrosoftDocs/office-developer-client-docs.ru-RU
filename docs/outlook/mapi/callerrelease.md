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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет функцию вызова, которая может освободить объект данных таблицы при выпуске представления таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Определенные функции, реализованные в:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Определенная функция, вызванная:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Parameters

 _ulCallerData_
  
> [in] Данные вызываемого звонка, сохраненные MAPI с представлением таблицы и переданы в функцию callback на основе **CALLERRELEASE.** Данные предоставляют контекст о выпущенной таблице представления. 
    
 _lpTblData_
  
> [in] Указатель на [интерфейс ITableData : IUnknown](itabledataiunknown.md) для объекта данных таблицы, в соответствии с выпущенным представлением таблицы. 
    
 _lpVue_
  
> [in] Указатель на [интерфейс IMAPITable : IUnknown](imapitableiunknown.md) для выпуска представления таблицы. Это интерфейс для объекта таблицы, возвращаемого в  _параметре lppMAPITable_ метода [ITableData::HrGetView,](itabledata-hrgetview.md) который создал объект для выпуска. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет 
  
## <a name="remarks"></a>Примечания

Клиентские приложения или поставщик услуг, заполнив объект данных таблицы, могут вызвать [ITableData::HrGetView,](itabledata-hrgetview.md) чтобы создать представление таблицы только для чтения. Вызов в **HrGetView** передает указатель на функцию вызова callback на основе **CALLERRELEASE,** а также контекст, который необходимо сохранить с помощью представления таблицы. Когда отсчет ссылок представления таблицы возвращается к нулю и представление будет выпущено, реализация **IMAPITable** вызывает функцию обратного вызова, передав контекст в _параметре ulCallerData._ 
  
Обычной функцией callback на основе **CALLERRELEASE** является освобождение объекта данных с базирующейся таблицей и не нужно отслеживать его во время последующей обработки. 
  

