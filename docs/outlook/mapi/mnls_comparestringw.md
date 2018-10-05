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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396213"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнение двух строк Юникод.
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a>Параметры

 _lcid_
  
> [in] Идентификатор языкового стандарта. Параметр _Locale_ [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)подробные определения см.
    
 _dwFlags_
  
> [in] Флаги, следует ли игнорировать регистр и диакритические знаки. Подробные определения в разделе параметр _dwCmpFlags_ [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Указатель для первой строки Юникод для сравнения.
    
 _cch1_
  
> [in] Длина в символах первой строки Юникод, за исключением конечный символ null. Приложение может предоставлять отрицательным значением, если строка символом null. В этом случае функция **MNLS_CompareStringW** определяет продолжительность автоматически. 
    
 _pstr2_
  
> [in] Указатель на втором строку в кодировке Юникод для сравнения.
    
 _cch2_
  
> [in] Длина в символах второй строки Юникод, за исключением конечный символ null. Приложение может предоставлять отрицательным значением, если строка символом null. В этом случае функция определяет продолжительность автоматически.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает значения, описанного для [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Замечания

Эта функция является [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** принимает те же параметры и имеет то же самое, что и [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

