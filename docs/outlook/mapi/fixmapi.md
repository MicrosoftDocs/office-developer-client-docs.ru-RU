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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает копию резервного копирования текущей копии mapi32.dll на клиентском компьютере и восстанавливает mapi32.dll с помощью библиотеки mapistub.dll.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируемая по:  <br/> |mapistub.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Возвращаемые значения

Если функция будет успешной, возвращаемая сумма не будет нулевой.
  
Если функция не работает, возвращается значение ноль. Чтобы получить расширенные сведения об ошибках, позвоните в функцию Microsoft Windows Software Development Kit (SDK) **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Примечания

 **FixMAPI** не заменяет текущий файл mapi32.dll, если файл помечен как только для чтения. 
  
 **FixMAPI** не заменяет текущий mapi32.dll, Microsoft Exchange Server установлен на компьютере. 
  
Когда **FixMAPI** создает копию резервного копирования текущей копии mapi32.dll на компьютере, она назначает копию резервной копии имя, отличаее от "mapi32.dll". Затем он направляет последующие вызовы, предназначенные для этой сборки, в копию резервного копирования. 
  
## <a name="see-also"></a>См. также



[KB 256946. При запуске Outlook 2000 г. вы получаете сообщение об ошибке конфликта программы](https://support.microsoft.com/kb/256946)
  
[KB 228457: Описание средства Fixmapi.exe, включенного в Internet Explorer 5](https://support.microsoft.com/kb/228457)

