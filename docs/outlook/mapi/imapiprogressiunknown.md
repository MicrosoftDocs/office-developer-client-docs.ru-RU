---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419648"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Реализует объект progress, который обеспечивает клиентские приложения индикатором прогресса. Индикатор прогресса — это дисплей пользовательского интерфейса, отображающий процент завершения операции, например копирование папок между хранилищами сообщений. MAPI и клиентские приложения реализуют объекты прогресса, и поставщики услуг используют их. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Объекты хода выполнения  <br/> |
|Реализовано в:  <br/> |MAPI и клиентские приложения  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIProgress  <br/> |
|Тип указателя:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Обновляет индикатор прогресса с отображением прогресса по мере выполнения операции.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Возвращает параметры флага из объекта progress для уровня операции, на котором рассчитывается информация о ходе выполнения.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Возвращает максимальное количество элементов в операции, для которой отображаются сведения о ходе выполнения.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Возвращает минимальное значение в [методе SetLimits,](imapiprogress-setlimits.md) для которого отображаются сведения о ходе выполнения.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Задает нижние и верхние ограничения для количества элементов в операции и флагов, которые контролируют, как вычисляется информация о ходе операции.  <br/> |
   
## <a name="remarks"></a>Примечания

MAPI включает  _параметр lpProgress_ во многих методах, которые выполняют потенциально длительные операции.  _lpProgress_ указывает на клиентскую реализацию объекта progress. Клиенты, реализуют **интерфейс IMAPIProgress,** задан этот параметр, чтобы указать на их реализацию; клиенты, которые не **реализуют IMAPIProgress,** устанавливают параметр NULL. Чтобы отобразить индикатор прогресса во время обработки операции, поставщики служб используют объект progress, предоставленный клиентом, при наличии, или реализацию MAPI (указывается, когда  _lpProgress_ задается NULL). 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Files**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MapiProgress.h и MapiProgress.cpp  <br/> |Неприменимо  <br/> |Если параметр IMAPIProgress включен, MFCMAPI передает **реализацию IMAPIProgress** всем функциям, вызываемым MFCMAPI, которые принимают реализацию.  <br/> |
   
## <a name="see-also"></a>См. также



[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы MAPI](mapi-interfaces.md)

