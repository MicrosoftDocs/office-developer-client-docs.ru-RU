---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439998"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает атрибуты свойств объекта [iMessage](imessageimapiprop.md) , предоставляемого функцией [опенимсгонистг](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики хранилищ сообщений  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Параметры

 _Лпобжект_
  
> возврата Указатель на объект **iMessage** , полученный из функции [опенимсгонистг](openimsgonistg.md) . 
    
 _Лппроптагаррай_
  
> возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , содержащую массив тегов свойств, указывающий свойства, для которых необходимо извлечь атрибуты. 
    
 _Лпппропаттраррай_
  
> вышли Указатель на указатель на возвращенную структуру [спропаттраррай](spropattrarray.md) , содержащую атрибуты извлеченных свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
МАПИ_В_ЕРРОРС_РЕТУРНЕД 
  
> Вызов выполнен в целом, но не удалось получить доступ к одному или нескольким свойствам и они возвращались с типом свойства ПТ_ЕРРОР.
    
## <a name="remarks"></a>Примечания

Доступ к атрибутам свойств возможен только для объектов Property, то есть объектов, реализующих интерфейс [IMAPIProp: IUnknown](imapipropiunknown.md) . Чтобы сделать свойства MAPI доступными в объекте структурированного хранилища OLE, [опенимсгонистг](openimsgonistg.md) создает объект [iMessage: IMAPIProp](imessageimapiprop.md) в начале объекта OLE **IStorage** . Атрибуты свойств таких объектов можно задавать или изменять с помощью [сетаттрибимсгонистг](setattribimsgonistg.md) и извлекаются с помощью **жетаттрибимсгонистг**. 
  
> [!NOTE]
> **Жетаттрибимсгонистг** и **сетаттрибимсгонистг** не работают со всеми объектами **iMessage** . Они действительны только для объектов **iMessage**— On — **IStorage** , возвращаемых методом **опенимсгонистг**. 
  
Число и позиции атрибутов в параметре _лпппропаттраррай_ соответствуют числу и положениям тегов свойств в параметре _лппроптагаррай_ . 
  

