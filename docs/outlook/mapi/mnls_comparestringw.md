---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Последнее изменение: 20 февраля 2012 г.'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356849"
---
# <a name="mnls_comparestringw"></a>MNLS_CompareStringW

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает две строки Юникод.
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a>Parameters

 _lcid_
  
> [in] Идентификатор locale. Подробные определения см. в _параметре Locale_ [compareString.](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
    
 _dwFlags_
  
> [in] Флаги для игнорирования дела и диакритики. Подробные определения см. в _параметре dwCmpFlags_ [compareStringEx.](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)
    
 _pstr1_
  
> [in] Указатель на первую строку Юникод для сравнения.
    
 _cch1_
  
> [in] Длина символов первой строки Юникод, за исключением завершаемого null-символа. Приложение может предоставить отрицательное значение, если строка не завершена. В этом случае функция **MNLS_CompareStringW** определяет длину автоматически. 
    
 _pstr2_
  
> [in] Указатель на вторую строку Юникод для сравнения.
    
 _cch2_
  
> [in] Длина символов второй строки Юникод, за исключением завершаемого null-символа. Приложение может предоставить отрицательное значение, если строка не завершена. В этом случае функция определяет длину автоматически.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает значения, описанные для [CompareStringEx.](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)
  
## <a name="remarks"></a>Примечания

Эта функция [обертывания CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** принимает те же параметры и имеет такое же поведение, как [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

