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
  
Создает резервную копию текущей копии MAPI32. dll на клиентском компьютере и восстанавливает MAPI32. dll с помощью библиотеки заглушек MAPI, мапистуб. dll.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировано:  <br/> |мапистуб. dll  <br/> |
|Вызывающая сторона:  <br/> |Client  <br/> |
|Реализовано в:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Возвращаемые значения

Если функция выполнена успешно, возвращаемое значение — ненулевое значение.
  
Если функция завершается с ошибкой, возвращается нулевое значение. Чтобы получить расширенные сведения об ошибке, вызовите функцию пакета средств разработки программного обеспечения (SDK) Microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Примечания

 **Фиксмапи** не заменяет текущий файл MAPI32. dll, если он имеет атрибут "только для чтения". 
  
 **Фиксмапи** не заменяет текущую библиотеку mapi32. dll, если на компьютере установлен Microsoft Exchange Server. 
  
Когда **фиксмапи** создает резервную копию текущей копии MAPI32. dll на компьютере, она назначает имя резервной копии, отличному от "MAPI32. dll". Затем он направляет последующие вызовы, предназначенные для этой сборки, в резервную копию. 
  
## <a name="see-also"></a>См. также



[Статья базы знаний 256946: при запуске Outlook 2000 появляется сообщение об ошибке "конфликт программ"](https://support.microsoft.com/kb/256946)
  
[Статья базы знаний 228457: Описание средства Фиксмапи. exe, включенного в Internet Explorer 5](https://support.microsoft.com/kb/228457)

