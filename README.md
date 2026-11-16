# @dstha/debounce

A lightweight TypeScript React hook for debouncing values.

## Installation

```bash
npm install @dstha/debounce
```

## Usage

```tsx
import { useState } from 'react';
import { useDebounce } from '@dstha/debounce';

export function SearchInput() {
    const [query, setQuery] = useState('');
    const debouncedQuery = useDebounce(query, 300);

    return (
        <input
            value={query}
            onChange={(e) => setQuery(e.target.value)}
            placeholder="Search..."
        />
    );
}
```