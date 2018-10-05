---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383816"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Делает резервную копию текущего копию mapi32.dll на стороне клиента, компьютер и восстанавливает mapi32.dll с библиотекой заглушка MAPI, mapistub.dll.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |MAPISTUB.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |"Windows";  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Возвращаемые значения

Если функция успешно выполнена, возвращается ненулевое значение.
  
Если функция завершается с ошибкой, возвращаемое значение равно нулю. Чтобы получить расширенные сведения об ошибке, вызовите функцию комплект разработки программного обеспечения (SDK) Windows Microsoft, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Замечания

 **FixMAPI** не заменяет текущий файл mapi32.dll, если файл помечен как доступный только для чтения. 
  
 **FixMAPI** не заменяет текущий mapi32.dll, если на компьютере установлен Microsoft Exchange Server. 
  
Когда **FixMAPI** создает резервную копию текущего копию mapi32.dll на компьютере, назначает резервной копии имя, отличное от «mapi32.dll». Затем переходит последующих вызовов, предназначенный для этой сборке для резервной копии. 
  
## <a name="see-also"></a>См. также



[Статья БАЗЫ знаний 256946:, Вы получаете сообщение об ошибке конфликта программы при запуске Outlook 2000](https://support.microsoft.com/kb/256946)
  
[Статья БАЗЫ знаний 228457: Описание средства Fixmapi.exe входит в состав Internet Explorer 5](https://support.microsoft.com/kb/228457)

