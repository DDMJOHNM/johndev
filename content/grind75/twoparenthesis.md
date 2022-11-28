---
title: "Grind 75 -Two Parenthesis"
date: 2022-10-18T16:56:59+13:00
draft: true
---

```
func isValid(s string) bool {

	for i, c := range s {
		if i < len(s)-1 {
			sc := fmt.Sprintf("%c", c)
			closing := fmt.Sprintf("%c", s[i+1])
			switch sc {
			case "(":
				if closing != ")" {
					return false
				}
			case "[":
				if closing != "]" {
					return false
				}
			case "{":
				if closing != "}" {
					return false
				}
			}
		}
	}

	return true
}

```