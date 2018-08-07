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
ms.openlocfilehash: 3c064301a18a8adbfb6109170ed16cb6981d96c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808435"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Относится к**: Outlook 
  
Делает резервную копию текущего копию mapi32.dll на стороне клиента, компьютер и восстанавливает mapi32.dll с библиотекой заглушка MAPI, mapistub.dll.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |MAPISTUB.dll  <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Реализованный:  <br/> |"Windows";  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Возвращаемые значения

Если функция успешно выполнена, возвращается ненулевое значение.
  
Если функция завершается с ошибкой, возвращаемое значение равно нулю. Чтобы получить расширенные сведения об ошибке, вызовите функцию комплект разработки программного обеспечения (SDK) Windows Microsoft, **[GetLastError](http://msdn.microsoft.com/en-us/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Замечания

 **FixMAPI** не заменяет текущий файл mapi32.dll, если файл помечен как доступный только для чтения. 
  
 **FixMAPI** не заменяет текущий mapi32.dll, если на компьютере установлен Microsoft Exchange Server. 
  
Когда **FixMAPI** создает резервную копию текущего копию mapi32.dll на компьютере, назначает резервной копии имя, отличное от «mapi32.dll». Затем переходит последующих вызовов, предназначенный для этой сборке для резервной копии. 
  
## <a name="see-also"></a>См. также



[Статья БАЗЫ знаний 256946:, Вы получаете сообщение об ошибке конфликта программы при запуске Outlook 2000](http://support.microsoft.com/kb/256946)
  
[Статья БАЗЫ знаний 228457: Описание средства Fixmapi.exe входит в состав Internet Explorer 5](http://support.microsoft.com/kb/228457)

