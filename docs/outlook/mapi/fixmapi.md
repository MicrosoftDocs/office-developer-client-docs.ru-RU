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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334963"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает резервную копию текущей копии mapi32.dll на клиентском компьютере и восстанавливает mapi32.dll с помощью библиотеки загона MAPI, mapistub.dll.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируется с помощью:  <br/> |mapistub.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Возвращаемые значения

В случае успешного функционирования функции возвращаемая величина не является нулем.
  
Если функция не работает, возвращается нулевое значение. Чтобы получить расширенные сведения об ошибках, вызовите функцию Microsoft Windows Software Development Kit (SDK) **[GetLastError.](https://msdn.microsoft.com/library/ms679360.aspx)** 
  
## <a name="remarks"></a>Примечания

 **FixMAPI** не заменяет текущий файл mapi32.dll, если он помечен как "только для чтения". 
  
 **FixMAPI** не заменяет текущий mapi32.dll если Microsoft Exchange Server установлен на компьютере. 
  
Когда **FixMAPI** создает резервную копию текущей копии mapi32.dll на компьютере, он присваивает резервной копии имя, которое отличается от "mapi32.dll". Затем он направляет последующие вызовы, предназначенные для этой сборки, в резервную копию. 
  
## <a name="see-also"></a>См. также



[KB 256946: при запуске Outlook 2000 вы получаете сообщение о конфликте программы](https://support.microsoft.com/kb/256946)
  
[KB 228457: описание средства Fixmapi.exe, включенного в Internet Explorer 5](https://support.microsoft.com/kb/228457)

