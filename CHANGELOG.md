# 0.1.1

* Use backup.lpop instead of backup.del

# 0.1.0

* `Ost#each` no longer rescues exceptions for you.

    You are in charge of rescuing and deciding what to do.

* You can inspect the status of the queue by calling `Ost::Queue#items`.

* If you need access to the underlying Redis key, it's in `Ost::Queue#key`.

* Ost now uses `BRPOPLPUSH` and maintains a backup queue while working.

    You can access this queue using `Ost::Queue#backup`.
